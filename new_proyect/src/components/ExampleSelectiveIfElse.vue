<template>
    <h1 v-if="age<18"> ERES MENOR DE EDAD</h1>
    <h1 v-else> ERES MAYOR DE EDAD</h1>
</template>

<script lang="ts" setup>
    let age= 20
</script>

<style scoped>
</style>