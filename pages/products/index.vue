<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
                <!--colocar : em product para o valor ser dinâmico-->
                <ProductCard :product="p" />
            </div>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })

    const { data: products } = await useFetch('https://fakestoreapi.com/products')

    useHead({
        title: 'Nuxt Elden | S',
        meta: [{
            name: 'description', content: 'Nuxt 3 Merch'
        }]
    })
</script>

<style scoped>

</style>