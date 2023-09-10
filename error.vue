<template>
    <div class="mt-7 max-w-sm mx-auto text-center card">
        <p class="mt-7 text-7x1 font-bold">{{ error.statusCode }}</p>
        <p class="mt-7 text-6-1">Ooops.</p>
        <P class="mt-7">{{ error.message }}</P>
        <button class='btn my-7' @click="handleClearError">Home...</button> 
    </div>
</template>

<script setup>
    defineProps(['error'])

    //Essa função limpa o erro e redireciona apara a página home
    const handleClearError = () => clearError({redirect: '/'})
</script>

<style scoped>

</style>