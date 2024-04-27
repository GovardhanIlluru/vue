<template>
  
    <div class="container">
    <h2>Movie Showtime:</h2>
    <div class="details">{{ book.movie_showtime }}</div>
    <h2>Movie Details:</h2>
    <div class="details">{{ book.movie_details }}</div>
    <h2>Location:</h2>
    <div class="details">{{ book.Location }}</div>
    <h2>Screening Rooms</h2>
    <div class="details">{{ book.Screening_rooms }}</div>

  </div>

</template>
<script>

export default {
    name: 'SingleBook',
    props:{
        book: Array
    }
    
}

// const bigbox=document.querySelector('.div')
// bigbox.addEventListener('mouseover',()=>{ 
//     bigbox.textContent=" Just got clicked";
// })
</script>

<style scoped>
.green{
  background-color: #3da35d;
  width: 40%;
  margin: 10px auto
  ;}

h4{
  margin: 2px
}
.container {
    display: grid;
    grid-template-columns: max-content auto;
    row-gap: 10px;
    padding: 15px;
    gap: 30px;
    justify-content: center;
    align-items: center;
    margin-bottom: 50px;
    background-color: lightblue;
}


h2 {
        text-align: right;
        margin: 0;
        font-size: medium;
    }

.details {
        text-align: left;  
    }


@media screen and (max-width: 768px) {
  .container {
    display: grid;
    height: auto;
    grid-template-columns: max-content auto;
  }

  .green,.red {
    width: 80%; 
    
  }
 
}
</style>
