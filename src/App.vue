<template>

  <MyHeader Name="PATHOGENESIS" authorName="Pathogenesis is the process by which a disease manifest" />
  <DiseaseName :patho=patho />

</template>

<script>

import MyHeader from './components/MyHeader.vue'
import DiseaseName from './components/DiseaseName.vue'

export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    DiseaseName
  },
  data(){
    return {
      patho: []
    }
  },
  methods:{
    //promoises
    async fetchpatho(){
      const res = await fetch('https://plum-creepy-coati.cyclic.app/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.patho = await this.fetchpatho();
  }

  // data() => this.data books
  // method => this.method => fetchbook
  // life cycle hooks created() => call our method here

}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>

