<template>
    <div class="bg-color-primary-light">
        <div class="container py-20 ">
            <div class="text-center m-auto mb-20 md:w-1/2 ">
                <h4 class="font-bold text-color-secondary mb-4">Our Feature</h4>
                <h1 class="title">Easy To Manage All Payments By Our App</h1>
            </div>

            <div class="grid lg:grid-cols-3 md:grid-cols-2 gap-12 lg:gap-8 px-4 sm:px-6
            lg:px-8 ">
                <!--Card number 1-->
                <div v-for="card in cards" class="border-2 border-solid border-color-gray text-center py-20 px-5
                rounded-2xl cursor-pointer hover:bg-color-primary-dark ease-in duration-200">
                    <div class="bg-color-secondary inline-block rounded-2xl py-5 px-6 ">
                        <i :class="card.icon"></i>
                    </div>
                    <h3 class="text-xl font-semibold py-4 ">{{card.title}}</h3>
                    <p class="leading-relaxed ">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequuntur aut rerum ut nulla possimus, vel eaque</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
    const cards = [
        {
            'title':'Every Day',
            'description':'Card description',
            'icon':'ri-calendar-2-fill text-white text-4xl'
        },
        {
            'title':'More Security',
            'description':'Card description',
            'icon':'ri-secure-payment-line text-white text-4xl'
        },
        {
            'title':'Hold World',
            'description':'Card description',
            'icon':'ri-global-line text-white text-4xl'
        }
    ];
</script>