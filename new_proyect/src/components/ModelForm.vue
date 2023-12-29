<template>
    <form>
        <input type="text" v-model="inputText"/>
        <input type="checkbox" v-model="agree"/> Acepto los terminos y condiciones de uso
        <select v-model="country">
            <option value="Venezuela">Venezuela</option>
            <option value="Colombia">Colombia</option>
            <option value="Francia">Francia</option>
            <option value="Estados Unidos">Estados Unidos</option>

        </select>
    </form>
    <h3>{{inputText}}</h3>
</template>

<script lang="ts" setup>
    import {ref} from 'vue'
     let inputText= ref('')
     let agree=ref(true)
     let country=ref('Venezuela')
</script>

<style scoped>

</style>