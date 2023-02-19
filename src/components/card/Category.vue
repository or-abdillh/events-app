<template>
    <section class="hover:bg-gray-700 active:scale-90 duration-300 flex items-center gap-3 px-3 py-4 min-w-[45%] rounded-2xl border border-gray-700 bg-gray-800">
        <!-- icon -->
        <section>
            <div class="h-10 w-10 bg-gray-200 rounded-xl grid place-items-center text-red-700"><i :class="props.icon"></i></div>
        </section>
        <!-- copywriter -->
        <section class="text-gray-300">
            <p class="leading-4 font-medium">{{ props.title }}</p>
            <small class="font-light">{{ props.amount }} events</small>
        </section>
    </section>
</template>

<script setup>

const props = defineProps({
    title: {
        type: String,
        default: 'Concerts'
    },
    amount: {
        type: Number,
        default: 17
    },
    icon: {
        type: String,
        default: 'fa-solid fa-ticket'
    }
})

</script>