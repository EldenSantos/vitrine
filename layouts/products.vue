<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4">
                <nuxtLink to="/products" class="font-bold">Nuxt</nuxtLink>
            </nav>
        </header>
        <!--saída do conteúdo da página-->
        <div class="container mx-auto p-4">
          <slot />
        </div>
        <footer class="container mx-auto p-4 flex justify-between border-t-2">
                <ul class="flex gap-4">
                    <li><nuxtLink to="/">Início</nuxtLink></li>
                    <li><nuxtLink to="/about">Sobre</nuxtLink></li>
                    <li><nuxtLink to="/products">Produtos</nuxtLink></li>
                </ul>
        </footer>
    </div>
  </template>
  
  <script setup>
  
  </script>
  
  <style scoped>
    .router-link-exact-active{
      color: #12b488;
    }
  </style>