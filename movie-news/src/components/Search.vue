<template>
    <h1>Search for specific news</h1>
    <div class="search-bar">
        <input type="text" class="search-input" placeholder="Enter movie topic">
        <span class="search-button"><img src="../assets/images/search.png" alt=""></span>
    </div>
    
</template>

<style scoped>
.search-input{
    font-family: 'Varela', sans-serif;
    font-size: 16px;
    justify-content: center;
    margin: 0 auto;
    display: flex;
    position: relative;
}

.search-button .search-bar{
    position: absolute;
    z-index: 2;
    display: block;
    width: 2.375rem;
    height: 2.375rem;
    line-height: 2.375rem;
    text-align: center;
    pointer-events: none;
    color: #aaa;
}
  

/* .search-container{
    background-color: #f2f2f2;

} */

/* .seach-bar > img{
    max-width: 30px;
    padding: 0.2em;
} */
    
</style>

