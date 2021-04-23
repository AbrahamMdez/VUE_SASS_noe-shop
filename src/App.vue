<template>
  <div id="app">
    <div id="nav">
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');


  * {
    margin: 0;
    padding: 0; 
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
  }

  :root {
    --primary-color: #C1545A;
    --secondary-color: #F6F6F6;
    --color-icons: #ebb60b;
    --color-price: #ebb60b;
    --color-text-price: #252525;
    --text-color: #c9c9c9;
    --color-button: #252525;
    --font-family: 'Roboto', sans-serif;
  }
</style>
