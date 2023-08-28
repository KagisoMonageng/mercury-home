<template>
    <header>
        <div class="container flex place-items-center pt-0">
            <RouterLink to="/" ><img src="../assets/images/Mercury-home-ww.png" class="w-52" alt=""></RouterLink>
            <nav>
                <RouterLink to="/" class="main-link">Home</RouterLink>

                <Popover class="relative">
                    <PopoverButton class="focus:outline-none rounded-xl flex place-items-end"><span class="main-link">About Us</span></PopoverButton>
                    <PopoverPanel class="absolute z-10 right-0 w-40 py-3">
                        <div class="bg-white bg-opacity-50 backdrop-blur-sm rounded-xl flex flex-col py-4">
                            <RouterLink to="/about" class="menu-item px-4 mb-2">Our Vision</RouterLink>
                            <RouterLink to="/drive" class="menu-item px-4 mb-2">What drives us</RouterLink>
                            <RouterLink to="/stores" class="menu-item px-4 mb-2">Find a store?</RouterLink>
                        </div>
                    </PopoverPanel>
                </Popover>
                <RouterLink to="/contact" class="main-link">Contact Us</RouterLink>
            </nav>
        </div>
    </header>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { RouterLink } from 'vue-router';
</script>

<style lang="scss" scoped>
header {
    width: 100%;
    position: fixed;
    top: 0;
    background-image: linear-gradient(to bottom,#0000006e,transparent);
    @apply bg-opacity-30;

    & nav {
        width: 100%;
        display: flex;
        justify-content: flex-end;
        place-items: center;
        gap: 20px;
    }

    & .main-link {
        font-size: 18px;
        font-weight: 300;
        color: #fff;
        transition: all 0.5s ease-in-out;
        padding: 5px 10px;
        border-radius: 10px;
        &:hover{
            background-color: #ffffff85;
        }


    }

    & .menu-item {
        font-size: 17px;
        color: #fff;
        font-weight: 300;
        & :hover{
            color: #000;
        }
    }

}
</style>