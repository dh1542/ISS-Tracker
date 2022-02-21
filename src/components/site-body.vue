<template>

<div class="container">
     <Map :lat="latitude" :lng="longitude" />

     <div class="box">
        
       
        <p>Message: {{message}}</p>
        <p>Timestamp: {{timestamp}}</p>
        
        <p>Longitude: {{longitude}}</p>
        
        <p>Latitude: {{latitude}}</p>
        <button @click="callISS()">refresh</button>
        

    </div>
    


</div>
   
    

    
</template>

<script>
import Map from './google-map.vue'

export default {
    name: 'site-body',
    components:{
        Map,
        
    },
    data: function(){
        return{
            
            message: "success",
            timestamp: 0,
            latitude: 0,
            longitude: 0,
            country: "country"
            
            
        }
    },
    methods:{
        /** calls an API which returns time and coordinates of the ISS */
        async callISS(){
            let response = await fetch('http://api.open-notify.org/iss-now.json')
            let data = await response.json()
            console.log(data)
            this.message = data.message
            this.timestamp = data.timestamp
            this.longitude = data.iss_position.longitude
            console.log(this.longitude)
            this.latitude = data.iss_position.latitude

        }
    }
}
</script>

<style scoped>
.container{
    position: relative;
    text-align: center;
}
button{
        margin-top: 2%;
        margin-bottom:2%;
    }
    
</style>



