<template>
  <navbar />

<div class="page-grid">
  <div class="grid-item">
    <Maintitle />
    <Globegif />
  </div>

  <div class="grid-item">
    <Workercards />
  </div>


</div>

</template>

<script>
import Maintitle from './components/Title.vue';
import navbar from './components/navbar.vue';
import Globegif from './components/globe.vue';
import Workercards from './components/workers.vue'

export default {
  name: 'App',
  components: {
    navbar,
    Maintitle,
    Globegif,
    Workercards
  }
}
</script>

<style>
  :root {
    --text: hsl(210, 20%, 94%);
    --background: hsl(206, 35%, 9%);
    --primary: hsl(199, 51%, 51%);
    --secondary: hsl(157, 64%, 47%);
    --accent: hsl(177, 57%, 24%);
  }

body{
  width: 100vw;
  min-height: 2000px;
  height: fit-content;
  overflow-x: hidden;
  overflow-y: scroll;
  background-color: var(--background);
  margin: 0;
  padding: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  justify-content: center;
}

::-webkit-scrollbar{
  background-color: rgba(0, 0, 0, 0);
  width: 7px;
}

::-webkit-scrollbar-thumb{
  background-color: var(--primary);
  width: 100%;
  height: 25vh;
  border-radius: 3.5px
}

/* page layout */
.page-grid{
  display: grid;
  grid-template-columns: 1;
  grid-template-rows: 5;
  width: 80vw;
  margin-left: 10vw;
  height: auto;
  margin-top: 100px;
}


/* sectoin 1 */
.grid-item{
  grid-row: 1;
  font-size: xx-large;
  display: flex;
  flex-direction: row;
  gap: 20px;
  margin-top: 100px;
}

@media only screen and (max-width: 600px){
  .grid-item{
    flex-direction: column
  }
}

.epic-text{
   background: linear-gradient(120deg, var(--primary), var(--secondary));
   background-clip: text;
   -webkit-background-clip: text;
   -webkit-text-fill-color: transparent;
}

/* section 2 */

.grid-item:nth-child(2){
  grid-row: 2;
  display: flex;
  flex-direction: row;
  justify-content: space-around
}
</style>
