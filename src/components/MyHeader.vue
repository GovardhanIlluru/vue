<template>
    <div>
        
        <h2>{{ bookName }}</h2>
        <h3>{{ authorName }}</h3>
    </div>
</template>

<script>

export default{
    name:'MyHeader',
    props:{
        bookName: String,
        authorName: String
    }
}
</script>

<style>
div{
    text-align: center;
}

</style>