<template>
<div>
    Hello
</div>
</template>
  
<script setup lang="ts">
import { defineComponent  } from 'vue';
defineComponent({
    name:'CycleOption',

    
    created () {
        console.log('created')
    },

    mounted () {
        console.log('mounted')
    },

    updated () {
        console.log('Updated')
    },

    unmounted () {
        console.log('Unmounted')
    },

})
 
</script>

<style scoped>
</style>
      