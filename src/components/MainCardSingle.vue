<script setup>
import { faker } from '@faker-js/faker'

const recipeName = faker.lorem.words(3); // generating recipe name
const ingredients = faker.lorem.words(50)
const timeToCook = faker.datatype.number({ min: 20, max: 60 })
const cookingInstructions = faker.lorem.paragraph(4)
 

</script>

<template>
    <RouterLink :to="{ name: 'CardDetail', params: {id: username} }">
        <div class="border border-gray-500 rounded-lg shadow bg-gray-400 h-full">
            <img class="object-fill h-480 w-960 rounded-t-lg" v-bind:src="faker.image.urlLoremFlickr({category: 'food', height:480, width: 960})" />
            <div class="p-4">
                <p class="mb-2 text-2xl font-bold">{{ firstname }} {{ lastname }} </p>
                <p class="mb-3 font-normal text-gray-800">{{ jobtitle }} </p>
                <p class="mb-3 font-normal text-gray-800">{{ bio }}  </p> 
            </div>
        </div>
    </RouterLink>
</template>