<template>
<div class="post-card">
    <h3>Title</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin vehicula id diam eu molestie. Etiam a sodales augue. Phasellus euismod viverra est. Aenean at consectetur nisl, at sollicitudin purus. Maecenas nec dignissim lacus. Maecenas vehicula dui justo, at ullamcorper mi auctor ac. Praesent nisl risus, vulputate sit amet neque et, pellentesque molestie massa. In et nisi eu tortor feugiat pharetra. Donec a arcu suscipit, hendrerit augue quis, elementum ipsum. Nam a libero vulputate, rhoncus lacus at, faucibus tellus. Donec a facilisis mi. Integer placerat porttitor eros vel rutrum. Nunc pellentesque nec libero ac semper. Ut bibendum ultrices lectus. </p>
    <PostButtom/>
</div>
</template>

<script lang='ts' setup>
    import PostButtom from './PostButtom.vue';
</script>

<style scoped>
.post-card{
    border-radius: 15px;
    padding: 10px;
    margin:5px;
    border:1px solid #ccc;
}
</style>