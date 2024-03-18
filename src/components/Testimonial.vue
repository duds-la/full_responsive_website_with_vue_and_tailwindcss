<template>
    <div>
        <div class="container py-20">
            <div class="text-center m-auto mb-20 md:w-1/2 ">
                <h4 class="font-bold text-color-secondary mb-4">Our Clients</h4>
                <h1 class="title">Easy To Manage All Payments By Our App</h1>
            </div>
        </div>

        <!--Review Container-->
        <div class="mt-8 ">
            <div class="flex items-center justify-center flex-wrap">
                <img v-for="(faceUser, index) in faceUsersWithDuplicates" :key="index" :src="faceUser.src" :class="faceUser.class" alt="" @click="changeComment(index)">
            </div>

            <div class="grid place-items-center text-center m-auto md:w-4/5 min-h-[40vh]">
                <div v-for="(comentUser, index) in comentsUsers" :key="index" class="user-text" :class="{ 'hidden': selectedCommentIndex !== index }">
                    <p class="md:text-2xl mb-6">{{ comentUser.comment }}</p>
                    <h4 class="font-bold text-color-secondary mb-1">{{ comentUser.name }}</h4>
                    <p>{{ comentUser.job }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const faceUsers = [
    {
        src: "https://placehold.co/200x200",
        class: 'h-20 w-20 rounded-full p-1 m-3 user-pic'
    }
];

const faceUsersWithDuplicates = Array.from({ length: 2 }, () => faceUsers[0]);

const comentsUsers = [
    {
        comment:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Enim repudiandae excepturi debitis iusto exercitationem, explicabo dignissimos sapiente nam at culpa recusandae illum!',
        name: 'Warren',
        job: 'Developer'
    },    
    {
        comment:'1111 ipsum dolor, sit amet cons',
        name: '123',
        job: 'Developer'
    }
]

const selectedCommentIndex = ref(0);

function changeComment(index) {
    selectedCommentIndex.value = index;
    console.log(selectedCommentIndex.value,index)
}
</script>
