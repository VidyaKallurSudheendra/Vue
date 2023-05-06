<template>
    <div>
        <h1> {{Name}} </h1>
        <h4> {{authorName}} </h4>
    </div>
    </template>
        
    <script>
        
    export default{ // Exporting Default Object
        name: 'MyHeader',
        props:{ 
        
            Name:String,
            authorName:String    
        }
    }
        
    </script>
        
<style scoped>
        
div{
    text-align: center;
}
    
h1{
    color: #0000CD;
    padding: 10px;
    font-family: 'Noto Serif', serif;
    font-size: 80px;
}
    
h4{
    color: #f10e0e;
    padding: 10px;
    font-size: 20px;
}
    
</style>

