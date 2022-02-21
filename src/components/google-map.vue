<template>
<!--embed google map-->

    <div id="map"> </div>
    <button @click="print()">print</button>
    
        <!-- Async script executes immediately and must be after any DOM elements used in callback. -->
    
      
</template>

<script>



export default 
  {
    name: "google-map",
    props:{
        lat:Number,
        lng:Number,
    },
    data: function(){
        return{
            map: null,
            center: {lat:0,lng:0},

        }
    },
    methods:{
         /* eslint-disable no-undef */
        initMap(latitude, longitude){
            const position = {lat: latitude, lng: longitude};
            this.map = new google.maps.Map(document.getElementById('map'),
            {zoom: 4, center: position});

            const marker = new google.maps.Marker({
                position: position,
                map: map,
            });

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