<template>
    <div>
        <input type="number" v-model="subtotal"/>
        <h3>Total de impuestos a pagar: {{ totalVat }} ({{ vat }}%)</h3>

    </div>
    </template>
      
    <script lang="ts" setup>
        import {Ref, computed, ref } from 'vue';
        const vat= 21
        let subtotal:Ref<number>=ref(0)
        const totalVat= computed (() => (vat*subtotal.value)/100)

    

    </script>