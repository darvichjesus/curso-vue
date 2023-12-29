<template>
    <div>
        <p v-bind:style="{backgroundColor: '#ccc' , color:change}">El mensaje se ha enviado de forma satisfactoria</p>
        <button v-on:click="handleClick()">cambiar color</button>
    </div>
</template>

<script lang="ts" setup>
    import {ref} from 'vue'
    let change= ref('#fff')
    const handleClick = () => {change.value='#ff0000'}
</script>

<style scoped>

</style>