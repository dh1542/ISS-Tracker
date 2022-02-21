<template>
    <div id="header">
        <h1>{{title}}</h1>
        <p>{{text}}</p>
        <hr>
    </div>
    
</template>
<script>
export default {
    name: 'site-header',
    props:{
        title: String,
        text: String
    }
    
}
</script>

<style scoped>
hr{
    color: red;
    
}
</style>