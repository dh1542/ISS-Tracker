<template>
<!--embed google map-->
    <head>
        
    </head>
    <div id="map"> </div>
    <button @click="print()">print</button>
    
        <!-- Async script executes immediately and must be after any DOM elements used in callback. -->
    
      
</template>

<script>



export default 
  {
    name: "google-map",
    props:{
        lat:String,
        lng:String,
    },
    data: function(){
        return{
            map: null,
            center: {lat:58.5517,lng:26.2850},

        }
    },
    methods:{
         /* eslint-disable no-undef */
        initMap(){
            
             // The location of Uluru
            uluru = { lat: -25.344, lng: 131.036 };
            // The map, centered at Uluru
            map = new google.maps.Map(document.getElementById("map"), {
            zoom: 4,
            center: uluru,});

            



            
  

            

        },
        

        print(){
        console.log(this.lat, this.lng)
        },
    }
        
        
  
    

}
</script>

<style scoped>
#map{
    size:400px;
    width: 100px;
    
}
</style>