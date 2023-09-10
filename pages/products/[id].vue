<template>
    <div>
        <head>
            <title>Nuxt | {{ product.title }}</title>
            <meta name="description" :content="product.description" />
        </head>
        <ProductDetails :product="product" />
    </div>
</template>

<script setup>
    const { id } = useRoute().params
    const uri = 'https://fakestoreapi.com/products/' + id

    const { data: product } = await useFetch(uri)
    //caso ele só faça a primeira chamada usar o key com id do produto para ele considerar a chamada diferente
    //const { data: product } = await useFetch(uri, {key: idProduct})
    
    //verifica se o produto existe, se não existir ele cria um erro e redireciona para a página error.vue na raiz do projeto 
    if(!product.value){
        //fatal força o app a mostrar a página de erro caso o mesmo ocorra
        throw createError({ statusCode: 404, statusMessage: 'Produto não encontrado', fatal: true})
    }
    definePageMeta({
        layout: 'products'
    })
</script>

<style scoped>

</style>