<template>
    <header id="main-header" class="fixed inset-x-0 top-0 z-50">
        <nav class="relative flex items-center justify-between px-6 lg:px-8" aria-label="Global">
            <a id="scroller-trigger" class="absolute"></a>
            <div class="flex lg:flex-1">
                <RouterLink to="/home" class="-m-1.5 p-1.5">
                    <span class="sr-only">Mercury Home</span>
                    <img class="w-28 h-auto" src="../assets/images/Mercury-home-ww.png" alt="" />
                </RouterLink>
            </div>
            <div class="flex lg:hidden">
                <button type="button" class="-m-2.5 flex place-items-center justify-center rounded-md p-2.5"
                    @click="mobileMenuOpen = true">
                    <span class="sr-only">Open main menu</span>
                    <i class="fi fi-br-menu-burger icon icon-menu">&nbsp;</i>

                </button>
            </div>
            <div class="hidden lg:flex lg:gap-x-12">
                <RouterLink v-for="item in navigation" :key="item.name" :to="item.href"
                    class="text-sm font-normal leading-6 text-white">{{ item.name }}</RouterLink>
            </div>
            <div class="hidden lg:flex lg:flex-1 lg:justify-end">
                <RouterLink to="/login" class="text-sm font-semibold leading-6 text-white">Log in <span
                        aria-hidden="true">&rarr;</span></RouterLink>
            </div>
        </nav>
        <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
            <div class="fixed inset-0 z-50" />
            <DialogPanel
                class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
                <div class="flex items-center justify-between">
                    <RouterLink to="/home" class="-m-1.5 p-1.5">
                        <span class="sr-only">Mercury Home</span>
                        <img class="w-28" src="../assets/images/Mercury-home-bb.png" alt="" />
                    </RouterLink>
                    <button type="button" class="-m-2.5 flex place-items-center justify-center rounded-md p-2.5"
                        @click="mobileMenuOpen = false">
                        <span class="sr-only">Close menu</span>
                        <i class="fi fi-br-menu-burger icon icon-menu">&nbsp;</i>
                    </button>
                </div>
                <div class="mt-6 flow-root">
                    <div class="-my-6 divide-y divide-gray-500/10">
                        <div class="space-y-2 py-6">
                            <RouterLink v-for="item in navigation" :key="item.name" :to="item.href"
                                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">
                                {{ item.name }}</RouterLink>
                        </div>
                        <div class="py-6">
                            <RouterLink to="#"
                                class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">
                                Log in</RouterLink>
                        </div>
                    </div>
                </div>
            </DialogPanel>
        </Dialog>
    </header>
</template>

<script setup>
// import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { MenuIcon } from 'vue-feather-icons'
import { RouterLink } from 'vue-router';
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger);

const navigation = [
    { name: 'Home', href: '/' },
    { name: 'About Us', href: '/about' },
    { name: 'Branches', href: '/branches' },
    { name: 'Contact Us', href: '/contact-us' },
]

const mobileMenuOpen = ref(false);
</script>



<script>
import { onMounted } from 'vue';

export default {

    setup() {
            const header = document.getElementById("main-header")
            const scr_trigger = document.getElementById("scroller-trigger")

            console.log(header)
            window.addEventListener("scroll", (scroll) => {
                const scrollPosition = window.scrollY;
                console.log("Scroll position:", scrollPosition);

                if (scrollPosition > 0) {
                    header.classList.add("bg-added")
                } else {
                    header.classList.remove("bg-added")
                }
            })
    }

}



</script>

<style lang="scss" scoped>
header {
    transition: all 0.5s ease-in-out;
}

header.bg-added {
    background-color: #595957bf;
}
</style>