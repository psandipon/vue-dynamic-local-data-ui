<script setup lang="ts">
const props = defineProps({
    to: String,
})
</script>

<template>
    <div>
        <router-link
            :to="to"
            class="flex items-center text-sm py-4 px-6 h-12 overflow-hidden text-gray-700 text-ellipsis whitespace-nowrap hover:font-bold hover:text-gray-600 hover:bg-white transition duration-300 ease-in-out"
        >
            <slot name="icon"> </slot>
            <span>
                <span class="capitalize">
                    <slot name="text"> </slot>
                </span>
            </span>
        </router-link>
    </div>
</template>

<style scoped>
/**
    This class is attached by the vue router to detect currently active route
*/
a.router-link-exact-active {
    /* 
    @apply is to add tailwind css's classes.
    more at https://tailwindcss.com/docs/adding-custom-styles#adding-base-styles
    */
    @apply text-gray-900 bg-white border-l-4 pl-5 border-red-700 font-bold;
}
</style>
