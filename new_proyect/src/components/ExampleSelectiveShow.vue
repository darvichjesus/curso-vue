<template>
    <h1 v-show="age<18"> ERES MENOR DE EDAD</h1>
    <h1 v-show="age>=18"> ERES MAYOR DE EDAD</h1>
</template>

<script lang="ts" setup>
    let age= 17
</script>

<style scoped>
</style>