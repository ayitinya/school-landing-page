<script setup lang="ts">
import { Popover, PopoverButton, PopoverGroup, PopoverPanel } from '@headlessui/vue'

const links = [
    {
        name: 'Home',
        href: '/',
    },
    {
        name: 'About',
        href: '/about',
    },
    {
        name: 'Academics',
        href: '/academics',
    },
    {
        name: 'Admissions',
        href: '/admissions',
    },
    {
        name: 'Gallery',
        href: '/gallery',
    },
    {
        name: 'Staff',
        href: '/staff',
    },
    {
        name: 'Contact',
        href: '/contact',
    },
]

const hero = ref<HTMLElement | null>(null)
const navTransparent = ref(true)

onMounted(() => {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            navTransparent.value = entry.isIntersecting
        })
    }, {
        threshold: 0.9,
    })

    observer.observe(hero.value!)
})
</script>

<template>
    <div class="flex flex-col min-h-screen">
        <header class="z-50">
            <Popover class="fixed w-screen" :class="[navTransparent ? '' : 'bg-white drop-shadow']">
                <div class="mx-auto max-w-7xl px-4 sm:px-6">
                    <div class="flex items-center justify-between py-6 lg:justify-start lg:space-x-10">
                        <div class="flex justify-start lg:w-0 lg:flex-1">
                            <a href="#">
                                <span class="sr-only">Your Company</span>
                                <img class="h-8 w-auto sm:h-10"
                                    src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="" />
                            </a>
                        </div>
                        <div class="-my-2 -mr-2 lg:hidden">
                            <PopoverButton
                                class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                                :class="[navTransparent ? 'text-white' : '']">
                                <span class="sr-only">Open menu</span>
                                <Icon name="heroicons:bars-3" size="1.5rem" aria-hidden="true" />
                            </PopoverButton>
                        </div>
                        <PopoverGroup as="nav" class="hidden space-x-10 lg:flex">
                            <NuxtLink v-for="link in links" :key="link.name" :to="link.href"
                                class="text-base font-medium"
                                :class="[navTransparent ? 'text-white hover:text-gray-400' : 'text-gray-500 hover:text-gray-900']">
                                {{ link.name }}
                            </NuxtLink>
                        </PopoverGroup>
                        <div class="hidden items-center justify-end lg:flex lg:flex-1 lg:w-0">
                            <a href="#"
                                class="ml-8 inline-flex items-center justify-center whitespace-nowrap rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700">Contact
                                us</a>
                        </div>
                    </div>
                </div>

                <transition enter-active-class="duration-200 ease-out" enter-from-class="opacity-0 scale-95"
                    enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in"
                    leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
                    <PopoverPanel focus
                        class="absolute inset-x-0 top-0 origin-top-right transform p-2 transition lg:hidden">
                        <div
                            class="divide-y-2 divide-gray-50 rounded-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5">
                            <div class="px-5 pt-5 pb-6">
                                <div class="flex items-center justify-between">
                                    <div>
                                        <img class="h-8 w-auto"
                                            src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600"
                                            alt="Your Company" />
                                    </div>
                                    <div class="-mr-2">
                                        <PopoverButton
                                            class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                                            <span class="sr-only">Close menu</span>
                                            <Icon name="heroicons:x-mark" size="1.5rem" aria-hidden="true" />
                                        </PopoverButton>
                                    </div>
                                </div>
                            </div>
                            <div class="space-y-6 py-6 px-5">
                                <div class="grid grid-cols-2 gap-y-4 gap-x-8">
                                    <NuxtLink v-for="link in links" :key="link.name" :to="link.href"
                                        class="text-base font-medium text-gray-900 hover:text-gray-700">{{ link.name }}
                                    </NuxtLink>
                                </div>
                                <div>
                                    <a href="#"
                                        class="flex w-full items-center justify-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700">Contact
                                        us</a>
                                </div>
                            </div>
                        </div>
                    </PopoverPanel>
                </transition>
            </Popover>
            <div ref="hero" id="hero" class="h-[720px] max-h-screen">
                <div class="mx-auto max-w-7xl px-4 sm:px-6 h-full">
                    <div class="flex flex-col justify-end h-full py-16 lg:py-32 max-w-[50ch] md:max-w-[66ch]">
                        <h1 class="text-3xl tracking-tight font-extrabold text-white sm:text-4xl md:text-5xl">
                            <span class="block">A World Class </span>
                            <span class="block text-indigo-400 xl:inline">Educational Opportunity</span>
                        </h1>
                        <p class="mt-5 text-white text-lg sm:text-xl md:text-2xl">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus, quos.
                        </p>
                        <div>
                            <NuxtLink to="/about"
                                class="mt-8 inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10">
                                Contact Us
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </header>
        <main>
            <slot></slot>
        </main>
        <footer class="mt-auto bg-indigo-500/10">
            <div class="mx-auto max-w-7xl px-4 sm:px-6 pt-12">
                <div class="grid grid-cols-1 md:grid-cols-3">
                    <div>
                        <h3 class="text-xl my-3 font-semibold">Little Flower School</h3>
                        <address>
                            <p>1234 Main Street</p>
                            <p>Anytown, CA 12345</p>
                        </address>
                    </div>
                    <div>
                        <h3 class="text-xl my-3 font-semibold">
                            Office
                        </h3>
                        <address>
                            <a href="tel:123-456-7890">123-456-7890</a>
                        </address>
                        <time>Mon-Fri 8:00am-4:00pm</time>
                    </div>
                    <div>
                        <h3 class="text-xl my-3 font-semibold">Quick Links</h3>
                        <ul class="columns-1 sm:columns-2">
                            <li v-for="link of links">
                                <NuxtLink :to="link.href">{{ link.name }}</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="border-t border-gray-200 py-4 text-center text-sm text-gray-500">
                    <p class="">&copy; 2021 Your Company, Inc. All rights reserved.</p>
                </div>
            </div>
        </footer>
    </div>
</template>

<style scoped>
#hero {
    background-image: url('../assets/images/hero.jpg'), linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5));
    background-size: cover;
    background-repeat: no-repeat;
    background-blend-mode: overlay;
    background-position: center;
}

.router-link-active {
    @apply text-indigo-500 underline underline-offset-8;
}
</style>