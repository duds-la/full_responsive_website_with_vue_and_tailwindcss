<template>
    <div class="bg-color-primary-light">
        <div class="container py-20">
            <div class="text-center m-auto mb-20 md:w-1/2 ">
                <h4 class="font-bold text-color-secondary mb-4">How It Works</h4>
                <h1 class="title">Easy To Manage All Payments By Our App</h1>
            </div>

            <div class="flex flex-col items-center justify-between space-y-6 md:flex-row
            md:space-y-0 md:space-x-6">
                <!--Cards-->
                <div v-for="(card, index) in cards" :key="index" class="text-center cursor-pointer">
                    <div :class="card.class ? card.class : 'relative bg-color-primary-dark inline-block px-6 py-3 rounded-lg cursor-pointer hover:bg-color-secondary ease-in duration-200'" >
                        <p class="text-6xl">{{card.number}}</p>
                    </div>
                    <h3 class="text-xl font-semibold py-4 ">{{ card.title }}</h3>
                    <p class="leading-relaxed ">{{ card.description}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const cards = [
    {
        number: 1,
        title:"Install the App",
        description:"lorem ipsum dolor sit amet consectetur adipisicing elit and consectetur adipisicing",
        class:null,
    },
    {
        number: 2,
        title:"Setup Your Profile",
        description:"lorem ipsum dolor sit amet consectetur adipisicing elit and consectetur adipisicing",
        class: "relative inline-block px-6 py-3 rounded-lg cursor-pointer bg-color-secondary"
    },
    {
        number: 3,
        title:"Enjoy The Features",
        description:"lorem ipsum dolor sit amet consectetur adipisicing elit and consectetur adipisicing",
        class:null,
    },
]
</script>