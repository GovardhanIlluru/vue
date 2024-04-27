<template>
    <div>
        <h2>{{ movie_details }}</h2>

</div>
</template>

<script>

export default{
    name:'MyHeader',
    props:{
        movie_details: String,
        
    }
}
</script>

<style>
div{
    text-align: center;
}

</style>