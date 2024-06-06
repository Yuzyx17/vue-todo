<script setup lang="ts">


    const props = defineProps<{
        title: string,
        desc: string,
        check: boolean
    }>()

</script>

<template>
    <input type="checkbox" v-model="props.check" />
    {{ props.title }}
    {{ props.desc }}
    {{ props.check }}
    
</template>

<style scoped>

</style>