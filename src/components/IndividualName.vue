<template>
    

    <div>

                        <h2>{{patho.title}}</h2>
                        <h4> {{patho.description}}</h4>
                        <img class="image"  align-items=center :src="patho.imageURL" :alt="patho.title">
                        <h4> {{patho.types}}</h4>
                        <h4> {{patho.symptom}}</h4>
                        <h4> {{patho.cause}}</h4>
                        <h4> {{patho.treatment}}</h4>
                        <h4>Global Statistic:</h4><img class="image"  align-items=center :src="patho.global" :alt="patho.title">


    </div>
</template>

<script>

export default{
    name: 'IndividualName',
    props:{
        patho: Array
    }
}
</script>

<style scoped>

.green{
    background-color: green;
}

h4{
    margin: 2px;
    color: #000000;
    font-family: 'Times New Roman', Times, serif;
    font-size: 20px;
    text-align: justify;
    padding: 10px;
}

h2{
    margin: 2px;
    color: #DC143C;
    text-align: center;
    font-family: Castellar;
    font-size: 30px;
    padding: 10px;
}


.image{
    width: 400px;
    height: 200px;
}

div{
    background-color: #FFF8DC;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.red{
background-color: orangered !important;

}


</style>