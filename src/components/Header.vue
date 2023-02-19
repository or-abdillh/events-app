<template>
    <section class="flex items-center justify-between mb-5">
        <!-- copywriter -->
        <section>
            <p class="text-gray-400 text-sm">NOVEMBER 20, 9:31 PM</p>
            <h1 class="text-gray-300 text-3xl">Explore events</h1>
        </section>
        <!-- avatar -->
        <section>
            <div class="h-10 w-10 rounded-full grid place-items-center bg-gray-400"><i class="fa-solid fa-user"></i></div>
        </section>
    </section>
    <!-- Search Bar -->
    <SearchBar></SearchBar>
</template>

<script setup>

import SearchBar from '@/components/SearchBar.vue'

</script>