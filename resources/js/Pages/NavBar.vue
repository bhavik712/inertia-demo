<template>
    <div class="bg-gray-500">
        <div class="ml-10 px-20 py-1 flex items-baseline space-x-4">
            <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
            <Link
                href="/"
                class="my-2 rounded-md px-3 py-2 text-base font-medium hover:bg-gray-700 hover:text-white text-white"
                :class="{ 'bg-gray-900': isActive('home') }"
                >Home</Link
            >
            <Link
                href="/about"
                class="my-2 rounded-md px-3 py-2 text-base font-medium hover:bg-gray-700 hover:text-white text-white"
                :class="{ 'bg-gray-900': isActive('about') }"
                >About
            </Link>

            <Link
                href="/contact"
                class="my-2 rounded-md px-3 py-2 text-base font-medium hover:bg-gray-700 hover:text-white text-white"
                :class="{ 'bg-gray-900': isActive('contact') }"
                >Contact</Link
            >
        </div>
    </div>
</template>
<script setup>
import { Link } from "@inertiajs/vue3";

const props = defineProps({
    currentPage: String,
});
const isActive = (key) => key === props.currentPage;
</script>
<!-- <a href="/notes" class=" <?php applyNavStyle('/notes') ?> rounded-md px-3 py-2 text-base font-medium" >Notes</a> -->
