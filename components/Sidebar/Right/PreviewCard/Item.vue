<template>
    <div class='p-3 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300' :class='defaultTransition'>
        <slot></slot>
    </div>

</template>

<script setup>
const {defaultTransition, twitterBorderColor} = useTailwindConfig();
</script>