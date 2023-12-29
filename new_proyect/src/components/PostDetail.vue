<template>
<div class="post">
    <h3>{{props.title}}</h3>
    <p>{{ props.content }}</p>
    <input type="text" v-model="message"/>
    <button @click="handleClick">Di hola</button>
</div>
</template>
  
<script lang="ts" >
import { defineComponent } from 'vue';
import {Ref,ref} from 'vue'
export default defineComponent({
    name:'PostDetail',
    props: {
        title:{ type:String, required: true},content:{type: String, required: false, default: 'Este post no tiene contenido'}

    },
    emits:["sayHi"],
    setup (props,{emit}) {
        const handleClick = () => {
            emit('sayHi',message.value)
        }
        let message:Ref<string>=ref("")
        return{props,handleClick,message}

    }
})



 
</script> 
  
<style scoped>
.post {
    width: 310px;
    height: 200px;
    border-radius: 10px;
    background-color: greenyellow;
    margin: 5px;
}
</style>
  