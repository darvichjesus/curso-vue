<template>
    <p v-bind:class="{'danger' : Error}">El mensaje se ha enviado de forma satisfactoria</p>

</template>

<script lang="ts" setup>
    let Error=false;
</script>

<style scoped>
.danger {
    color: red;
}
</style>