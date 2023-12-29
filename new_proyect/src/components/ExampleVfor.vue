<template>
 <div>
    <ul>
        <li v-for="item in countries" v-bind:key="item">{{ item }}</li>
    </ul>
 </div>
</template>

<script lang="ts" setup>
    import {Ref,ref} from 'vue';
    let countries=ref([
        'Spain','France','UK','Portugal'
    ])

</script>

<style scoped>
</style>