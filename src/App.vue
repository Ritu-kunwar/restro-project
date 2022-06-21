<template>

<router-view />
</template>

<script>




export default {
    name: "App",
   
} 
</script>

<style>
body{
    padding: 0;
    margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}
.logo{
    width: 100px;
}
.register input , .login input , .add input
{
    width: 300px;
    height: 40px;
    display: block;
    padding-left: 20px;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 15px;
  
    border: 1px solid skyblue
    
}
.register button , .login button ,.add button
{
     width: 325px;
    height: 40px;
    border: 1px solid skyblue;
    color: white;
    background: skyblue;
    cursor: pointer;
}

</style>
