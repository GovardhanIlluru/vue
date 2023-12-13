<template>

  <!--Step 3 use the component-->
  <MyHeader bookName="Rental Properties near UNH" authorName="" yourName="Write your Name"/> 
  <BookBox :books=books />
 
</template>

<script>

// step 1 import the child component
import MyHeader from './components/MyHeader.vue'
import BookBox from './components/BookBox.vue'

// 

export default{
 name: 'App',
 // step 2: register the component 
 components:{
   MyHeader,
   BookBox
 },
 data(){
   return {
     books: []
   }
 },
 methods:{
   //promises
   async fetchbooks(){
     const res = await fetch("https://we-a4un.onrender.com/api");
     const data = await res.json()
     console.log(data)
     return data[0].books
   }
 },
 async created(){
   this.books = await this.fetchbooks();

 }

}

</script>
<style :global>
 body{
  font-family: sans-serif;
  background-color: #bee1e6;
 }
</style>
