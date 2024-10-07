<template>
    <div class='m-2 border rounded-2xl bg-gray-50 dark:bg-dim-700' :class='twitterBorderColor'>
        <h1>{{ props.title }}</h1>
    </div>
</template>
<script setup>
import {twitterBorderColor} from '~/composables/useTailwindConfig'
const props = defineProps({
    title:{
        type: String,
        required: true,
        // default: 'What\'s happening'
    }
})

</script>
