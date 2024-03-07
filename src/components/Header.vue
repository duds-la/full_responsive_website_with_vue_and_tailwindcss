<template>
    <div>
        <header>
            <nav class="container flex justify-between items-center">
                <div class="w-20 py-5 font-bold text-2xl">
                    <a href="#home" class="flex">Light <span class="text-color-secondary ml-1">CODE.</span></a>
                </div>
                <div class="">
                    <ul class="hidden lg:flex items-center space-x-6 ">
                        <li><a href="#home" class="hover:text-color-secondary ease-in duration-100">HOME</a></li>
                        <li><a href="#features" class="hover:text-color-secondary ease-in duration-100">FEATURES</a>
                        </li>
                        <li><a href="#blog" class="hover:text-color-secondary ease-in duration-100">BLOG</a></li>

                        <li>
                            <button
                                class="bg-color-secondary px-9 py-3 rounded-md capitalize font-semibold hover:opacity-85 ease-in duration-100">
                                FREE Trial</button>
                        </li>
                    </ul>
                </div>
                <!--MOBILE SCREEN-->
                <div id="hamburguer" class="lg:hidden cursor-pointer">
                    <i @click="openMenu" class="text-color-white ri-menu-3-line"></i>
                </div>

                <div id="close" v-if="aberto" class="lg:hidden cursor-pointer z-10">
                    <i @click="openMenu" class="text-color-white ri-close-line"></i>
                </div>
                <div id="menu" v-if="aberto" class=" bg-color-primary h-screen absolute inset-0">
                    <ul class="h-full grid place-items-center py-20 ">
                        <li><a href="#home" class="hover:text-color-secondary ease-in duration-100">HOME</a></li>
                        <li><a href="#features" class="hover:text-color-secondary ease-in duration-100">FEATURES</a>
                        </li>
                        <li><a href="#blog" class="hover:text-color-secondary ease-in duration-100">BLOG</a></li>

                        <li>
                            <button
                                class="bg-color-secondary px-9 py-3 rounded-md capitalize font-semibold hover:opacity-85 ease-in duration-100">
                                FREE Trial</button>
                        </li>
                    </ul>
                </div>
            </nav>
        </header>
    </div>
</template>
<script setup>
import { ref } from "vue";

const aberto = ref(false);

function openMenu() {
    aberto.value = !aberto.value;
    return aberto;
}
</script>
