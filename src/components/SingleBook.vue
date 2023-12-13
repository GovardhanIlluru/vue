<template>
    <div  :class="book.distance_to_unh_in_miles<=5 ? 'green' :'red ' " >
    <div class="container">
    <h2>Rental Number:</h2>
    <div class="details">{{ book.rental_number }}</div>
    <h2>Rental Description:</h2>
    <div class="details">{{ book.description }}</div>
    <h2>Renter Name:</h2>
    <div class="details">{{ book.renter }}</div>
    <h2>Distance from UNH:</h2>
    <div class="details">{{ book.distance_to_unh_in_miles }}</div>
    <h2>Address:</h2>
    <div class="details">{{ book.Address }}</div>
  </div>
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
    }

h2 {
        text-align: right;
        margin: 0;
        font-size: medium;
    }

.details {
        text-align: left;  
    }


.red{
  background-color: #ce4257;
  width: 40%;
  margin: 10px auto;
  
}

.green:hover{
background-color: #e8fccf;
transition-duration: 300ms;
  border-radius: 5px;
  scale: 105%;

}

.red:hover {
  background-color: #ffa69e;
  transition-duration: 300ms;
  border-radius: 5px;
  scale: 105%;

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
