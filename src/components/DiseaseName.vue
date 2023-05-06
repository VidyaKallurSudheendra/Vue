<template>
   
    
    <div v-for="patho of patho.patho" :key="patho.id" >

     
       <IndividualName :patho=patho />

    </div>

</template>
<script>
import IndividualName from './IndividualName.vue'

export default {
    name: 'DiseaseName',
    props:{
        patho: Array
    },
    components:{
        IndividualName
    }
    
}
</script>
<style scoped>


</style>
