<template>
    <div>
       <ul>
           <li v-for="item in countries" v-bind:key="item.name">{{ item.code }}</li>
       </ul>
    </div>
   </template>
   
   <script lang="ts" setup>
       import {Ref,ref} from 'vue';
       let countries=ref([
            {
                name:'es',
                code:'Spain'
            },
            {
                name:'en',
                code:'USA'
            },
            {
                name:'fr',
                code:'France'
            },

       ])
   
   </script>
   
   <style scoped>
   </style>