<template>
    <Header title="ISS Location Tracker" text="Where to find the International Space Station right now?"/>
    <Body />
</template>

<script>
import Header from './components/site-header.vue'
import Body from './components/site-body.vue'

export default {
  name: 'App',
  components: {
    Header,
    Body, 
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

.box{
  margin: auto;
  position: relative;
  text-align: center;
  
  width:37.5rem;
  height:7.5rem;
  border: 0.1rem dotted grey;
}



</style>
