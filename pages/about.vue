<script setup lang="ts">
definePageMeta({
  title: 'About',
  description: 'This is the about page',
  layout: false,
})
</script>

<template>
  <NuxtLayout name="default">
    <template #hero>
      <div id="hero" class="py-8">
        <div class="mx-auto max-w-7xl px-3 sm:px-6">
          <div class="flex flex-col justify-end h-full py-16 lg:py-32 max-w-[50ch] md:max-w-[66ch]">
            <h1 class="text-3xl tracking-tight font-extrabold text-white sm:text-4xl md:text-5xl">
              About <span class="text-indigo-400">Us</span>
            </h1>
          </div>
        </div>
      </div>
    </template>
    <div class="my-16 mx-auto max-w-7xl px-3 sm:px-6 flex flex-col sm:flex-row justify-end gap-4 lg:gap-8">
      <div class="basis-1/2">
        <h2
          class="text-2xl tracking-tight font-semibold sm:text-3xl md:text-4xl mb-4 text-indigo-500 underline underline-offset-8">
          Mission</h2>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quia quasi voluptatum fuga error magnam voluptate
          amet nulla ratione suscipit corporis.</p>
      </div>
      <div class="basis-1/2">
        <h2
          class="text-2xl tracking-tight font-semibold sm:text-3xl md:text-4xl mb-4 text-indigo-500 underline underline-offset-8">
          Vision</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nemo a ipsa fugit similique, provident
          consequuntur! Inventore, provident. Similique iure nemo suscipit enim dicta adipisci optio quia labore quaerat
          maxime, odio nam tenetur provident. Fugit officiis, ipsa illo expedita fugiat molestiae.</p>
      </div>
    </div>

    <div class="my-16 mx-auto max-w-7xl px-3 sm:px-6">
      <h2
        class="text-2xl tracking-tight font-semibold sm:text-3xl md:text-4xl mb-4 text-indigo-500 underline underline-offset-8">
        Our Story</h2>
      <p class="">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eveniet cumque fuga nulla delectus quod, temporibus
        sit illum sed tenetur facere, ratione omnis nostrum ad ullam voluptas repellat tempore ipsam molestiae? Iure
        quidem saepe voluptas, asperiores porro quo fugit fuga, sint quaerat placeat, deserunt ab laboriosam veniam
        adipisci. Ab, doloribus voluptatem reprehenderit, et facilis quae aperiam dolore consequuntur deleniti
        repudiandae unde exercitationem asperiores, odio tenetur dolorum voluptates minima nemo eum molestias! Vero
        eveniet iusto quia placeat quo, maxime facilis velit earum fugiat deleniti sit dolorem, delectus natus saepe ab,
        quas magni tenetur sed. Eligendi maxime quas deleniti quibusdam suscipit rem commodi?
      </p>
    </div>
  </NuxtLayout>
</template>

<style scoped>
#hero {
  background-image: url('../assets/images/hero-2.jpg'), linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5));
}
</style>