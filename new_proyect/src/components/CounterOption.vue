<template>
    <h3>{{ counter }}</h3>
    <button @click="AddCounter">Incrementar</button>
</template>

<script lang='ts'>
    import { defineComponent } from 'vue';
    export default defineComponent({
        name: "CounterOption" ,
        data() {
            let counter=0;
            return{counter}
        },
        methods: {
            AddCounter () {
                this.counter++
            }
        }
})
</script>

<style scoped>

</style>