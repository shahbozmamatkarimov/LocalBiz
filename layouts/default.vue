<template>
  <header>
    <Navbar />
    <div class="h-[40px]"></div>
    <div
      class="container md:py-16 sm:py-10 py-5 md:px-10 px-5 lg:mt-0 mt-10 mx-auto overflow-hidden"
    >
      <slot></slot>
    </div>
    <Footer />
  </header>
</template>

<script setup></script>

<style lang="scss" scoped></style>
