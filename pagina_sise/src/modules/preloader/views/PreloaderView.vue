<template>
    <div>
        <center>
            <img src="../../../assets/Logo.png">
        <LoaderComponent v-if="desactivarLoader"/>
        <h1 v-else>Loader desactivador</h1>
        </center>
        
    </div>
    
</template>
<script>
import LoaderComponent from '../components/LoaderComponent.vue';

export default{
    components: {
        LoaderComponent,
    },
    data(){
        return {
            desactivarLoader: true,
        }
    },

    methods:{
        quitarLoader(){

            setTimeout(()=>{
               let respuesta =  fetch('https://www.aseguradoraabank.com/', 'GET');
                console.log(respuesta)
               if(respuesta.length > 0){
                this.desactivarLoader = false;
               }
            
            }, 2000)
            
        },
    
        
    },

mounted(){
    this.quitarLoader();
}    
    
}
</script>

<style>

</style>