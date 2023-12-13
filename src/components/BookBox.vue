<template>
    <div>
        
        <div v-for="book of books" :key="book.rental_number" >
            <SingleBook :book=book />
        </div>

    </div>
    
       
</template>

<script>
import SingleBook from './SingleBook.vue'
export default{

    name:'BookBox',
    props:{
        books: Array
    },
    components:{
        SingleBook
    }

}

</script>
<style scoped>
div{
    text-align: center;
}
</style>