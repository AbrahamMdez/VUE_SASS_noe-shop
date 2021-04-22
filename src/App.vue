<template>
  <div id="app">
    <div id="nav">
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
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
    --color-icons: #C1545A;
    --input-color: #E3E3E3;
    --color-button: #DFBFC0;
    --font-family: 'Redressed', cursive;
  }
</style>
