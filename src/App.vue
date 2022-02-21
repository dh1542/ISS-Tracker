<template>
    <Header title="ISS Location Tracker" text="Where to find the International Space Station right now?"/>
    <Map />
</template>

<script>
import Header from './components/Header.vue'
import Map from './components/Map.vue'

export default {
  name: 'App',
  components: {
    Header,
    Map
  }
}
</script>

<style>
/** Import google font Roboto */
@import url('https://fonts.googleapis.com/css2?family=Roboto&family=Zen+Kaku+Gothic+Antique&display=swap');

html{
  font-family: roboto;
  background-color: white;
}

#header{
  

  text-align: center;
  padding: 1%;
  padding-bottom: 0;
  margin-bottom: 0;
  border: 1rem;
  
}
#header h1{
  margin-bottom: 0;
  
}

#header p{
  font-size: 90%;
  margin-top: 0;
  
}

#header hr{
  border-top: 1% solid red;
}

</style>
