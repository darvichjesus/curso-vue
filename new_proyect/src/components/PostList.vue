<template>
<div class="container">
    <post-detail v-for="elm in info" :key="elm.title" :title="elm.title" :content="elm.content" @sayHi="showAlert"/>
</div>
</template>
  
<script lang="ts" setup>
 import PostDetail from './PostDetail.vue';
 interface Post {
    title: string,
    content:string
 }


 let info:Array<Post>=[{title:'Este es el titulo', content:'Este es el contenido referente a la parte del post'},{title:'Este es el titulo 2', content:'Este es el contenido referente a la parte del post 2'},{title:'Este es el titulo 3', content:'Este es el contenido referente a la parte del post 3'},{title:'Este es el titulo 4', content:'Este es el contenido referente a la parte del post 4'},{title:'Este es el titulo 5', content:'Este es el contenido referente a la parte del post 5'}]
 function showAlert(msg=String) {
    alert(msg)
 }
</script>
  
<style scoped>
.container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-around;
    text-align: center;
}
</style>
  