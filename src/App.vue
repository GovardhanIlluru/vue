<template>

  <!--Step 3 use the component-->
  <MyHeader bookName="Movie Shows" authorName="" yourName="Write your Name"/> 
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
     const res = await fetch("https://node-ak4u.onrender.com/api");
     const data = await res.json()
     console.log(data)
     console.log("Adada")
     console.log(data[0].books)
     console.log("Data type of data[0].books:", typeof data[0].books);



     return data[0].books
   }
 },
 async created(){
  try {
    this.books = await this.fetchbooks();
  } catch (error) {
    console.error("Error fetching books:", error);
  }
   

 }

}

</script>
<style :global>
 body{
  font-family: sans-serif;
  background-color: #bee1e6;
 }
</style>
