<style scoped>

.no-ruler::-webkit-scrollbar {
    display: none;
}

</style>

<template>
    <main class="pb-24">
        <Header></Header>
        <!-- Popular events -->
        <section class="mt-8">
            <p class="text-gray-300 mb-3">POPULAR</p>
            <section class="flex gap-3 overflow-x-scroll no-ruler">
                <template v-for="card in 4" :key="card">
                    <CardEvent></CardEvent>
                </template>
            </section>
        </section>
        <!-- For you -->
        <section class="mt-8">
            <p class="text-gray-300 mb-3">FOR YOU</p>
            <CardBanner></CardBanner>
        </section>
        <!-- Categories -->
        <section class="mt-8">
            <p class="text-gray-300 mb-3">CATEGORIES</p>
            <section class="flex gap-3 overflow-x-scroll no-ruler">
                <template v-for="card in 4" :key="card">
                    <CardCategory></CardCategory>
                </template>
            </section>
        </section>
    </main>
    <BottomBar></BottomBar>
</template>

<script setup>

import Header from '@/components/Header.vue'
import BottomBar from '@/components/BottomBar.vue'
import CardEvent from '@/components/card/Event.vue'
import CardBanner from '@/components/card/Banner.vue'
import CardCategory from '@/components/card/Category.vue'

</script>