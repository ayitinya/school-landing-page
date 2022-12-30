<script setup lang="ts"></script>

<template>
  <div class="my-32 portrait:my-16 mx-auto max-w-7xl px-4 sm:px-6">
    <h1 class="my-8 text-5xl font-semibold">Hello world</h1>
    <p class="sm:columns-2 gap-12 lg:gap-20 lg:text-lg">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat temporibus quia, illum deserunt corrupti
      aperiam dolore, vel iusto itaque modi molestiae hic cumque suscipit reiciendis unde porro maxime rerum voluptate
      error ducimus tenetur velit? Architecto quas fugit recusandae reprehenderit adipisci reiciendis amet minus nisi
      omnis inventore dolor, illum consequatur nes
      <span class="block my-4">
        <NuxtLink to="/about"
          class="inline-flex items-center justify-center text-base font-medium md:text-lg underline underline-offset-4">
          Read More &rarr;
        </NuxtLink>
      </span>
    </p>
  </div>
  <div
    class="my-32 portrait:my-16 mx-auto max-w-7xl px-3 sm:px-6 flex flex-col items-center sm:flex-row  gap-8 justify-between">
    <NuxtLink class="h-96 w-72 rounded-lg relative flex justify-center overflow-hidden">
      <img src="https://picsum.photos/200/300" alt=""
        class="hover:brightness-50 hover:scale-125 origin-center object-cover h-full w-full">
      <span class="absolute bottom-0 my-4 bg-indigo-500/50 text-white text-center w-4/5  py-4" to="">
        Preschool
      </span>
    </NuxtLink>
    <NuxtLink class="h-96 w-72 rounded-lg relative flex justify-center overflow-hidden">
      <img src="https://picsum.photos/200/300" alt=""
        class="hover:brightness-50 hover:scale-125 origin-center object-cover h-full w-full">
      <span class="absolute bottom-0 my-4 bg-indigo-500/50 text-white text-center w-4/5  py-4" to="">
        Preschool
      </span>
    </NuxtLink>
    <NuxtLink class="h-96 w-72 rounded-lg relative flex justify-center overflow-hidden">
      <img src="https://picsum.photos/200/300" alt=""
        class="hover:brightness-50 hover:scale-125 origin-center object-cover h-full w-full">
      <span class="absolute bottom-0 my-4 bg-indigo-500/50 text-white text-center w-4/5  py-4" to="">
        Preschool
      </span>
    </NuxtLink>
  </div>

  <div
    class="my-32 portrait:my-16 mx-auto max-w-7xl px-4 py-8 sm:px-6 bg-indigo-500/10 flex flex-col items-center rounded-lg">
    <img src="https://picsum.photos/1080/400" class="w-full min-h-[250px] object-cover rounded-xl" alt="">
    <blockquote class="my-16">
      <span class="text-8xl font-serif text-indigo-500">"</span>
      <p class="mb-8 text-xl md:text-3xl lg:text-4xl font-light italic">
        Lorem ipsum dolor sit amet consectetur adipisicinosam velit veritatis! Atque animi hic ratione provident.
        Consectetur.
      </p>
      <p class="">
        <cite class="font-semibold">John Doe</cite>
      </p>
    </blockquote>
  </div>

  <div class="my-32 portrait:my-16 mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-center my-8 text-2xl font-semibold">Our School At A Glance</h2>
    <div class="flex flex-col sm:flex-row sm:flex-wrap items-center justify-between gap-12 lg:gap-20 lg:text-lg ">
      <div class="flex flex-col items-center">
        <span class="text-5xl font-bold text-indigo-500">2K+</span>
        <h3 class="my-4 text-xl font-semibold">Current Enrollments</h3>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-5xl font-bold text-indigo-500">90+</span>
        <h3 class="my-4 text-xl font-semibold">Qualified Tutors</h3>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-5xl font-bold text-indigo-500">90+</span>
        <h3 class="my-4 text-xl font-semibold">Qualified Tutors</h3>
      </div>
      <div class="flex flex-col items-center">
        <span class="text-5xl font-bold text-indigo-500">100%</span>
        <h3 class="my-4 text-xl font-semibold">Pass Rate</h3>
      </div>
    </div>
  </div>

  <div class="my-32 portrait:my-16 mx-auto max-w-7xl px-4 py-20 sm:px-6 bg-indigo-500">
    <h2 class="text-center my-8 text-2xl font-semibold text-white">
      Want to know more about admissions and upcoming events? Subscribe now!
    </h2>
    <form action="" class="flex flex-col sm:flex-row items-center justify-center">
      <input type="email" name="email" placeholder="username@provider.com" id="email"
        class="p-2 rounded w-4/5 sm:w-2/5">
      <button type="submit"
        class="border border-white text-white px-4 py-2 rounded-lg mt-4 sm:mt-0 sm:ml-4">Subscribe</button>
    </form>
  </div>

  <div class="my-32 portrait:my-16 mx-auto max-w-7xl px-4 sm:px-6">
    <h2 class="text-center my-8 text-2xl font-semibold">News And Updates</h2>
    <p>
      There is no news at the moment.
    </p>
  </div>
</template>