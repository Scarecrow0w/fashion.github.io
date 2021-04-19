<template>
  <div class="flex items-center justify-between w-full h-16 px-20 border">
    <div class="logo">
      <span class="font-serif text-2xl font-bold">FASHION</span>
      <div class="relative w-full border border-transparent bg-fgold opacity-30 logo-line"></div>
    </div>
    <div class="flex justify-between space-x-8 font-serif">
      <a class="hover:text-fgold text-fgold" href="/">Home</a>
      <a class="hover:text-fgold " href="/recipes">Recipes</a>
      <a class="hover:text-fgold " href="/article">Article</a>
      <a class="hover:text-fgold " href="/contact">Contact</a>
      <a class="hover:text-fgold " href="/purchase">Purchase</a>
    </div>
  </div>
</template>

<style scoped>
  .logo-line {
    height: 6px;
    bottom: 12px;
  }
</style>
