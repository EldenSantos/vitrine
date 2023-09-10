<template>
  <div>
      <header class="shadow-sm bg-white">
          <nav class="container mx-auto p-4 flex justify-between">
              <nuxtLink to="/" class="font-bold">Nuxt</nuxtLink>
              <ul class="flex gap-4">
                  <li><nuxtLink to="/">Início</nuxtLink></li>
                  <li><nuxtLink to="/about">Sobre</nuxtLink></li>
                  <li><nuxtLink to="/products" class="btn">Produtos</nuxtLink></li>
                  <li><nuxtLink to="/products/abc" class="btn">Produto abc</nuxtLink></li>
              </ul>
          </nav>
      </header>
      <!--saída do conteúdo da página-->
      <div class="container mx-auto p-4">
        <slot />
      </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
  .router-link-exact-active{
    color: #12b488;
  }
</style>