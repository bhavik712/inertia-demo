<template>
    <div class="bg-white shadow">
        <div class="ml-20 max-w-7xl px-10 py-6">
            <h1 class="text-3xl font-bold tracking-tight text-gray-900">
                {{ props.pageTitle }}
            </h1>
        </div>
    </div>
</template>
<script setup>
const props = defineProps({
    pageTitle: String,
});
</script>
