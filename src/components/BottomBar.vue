<style scoped>

.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}


</style>

<template>
    <!-- wrapper -->
    <section class="w-full fixed bottom-0 left-0 right-0">
        <!-- bottom bar -->
        <section class="lg:w-5/12 xl:w-4/12 lg:mx-auto bg-gray-900 flex justify-around py-6">
            <template v-for="bottom in bottoms" :key="bottom.name">
                <button @click="activeBottom = bottom.name">
                    <span v-if="activeBottom == bottom.name">
                        <p class="text-center text-sky-300 mb-1">{{ bottom.name }}</p>
                        <div class="h-2 w-2 bg-sky-300 rounded-full mx-auto"></div>
                    </span>
                    <i v-else class="text-gray-200 text-2xl" :class="bottom.icon"></i>
                </button>
            </template>
        </section>
    </section>
</template>

<script setup>

import { ref } from 'vue'

const activeBottom = ref('Explore')

const bottoms = [
    {
        name: 'Explore',
        icon: 'fa-solid fa-home'
    },
    {
        name: 'Events',
        icon: 'fa-solid fa-calendar'
    },
    {
        name: 'Tickets',
        icon: 'fa-solid fa-ticket'
    },
    {
        name: 'Setting',
        icon: 'fa-solid fa-gear'
    },
]

</script>