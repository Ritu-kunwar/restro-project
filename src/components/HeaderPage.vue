<template>
<div class="nav"> 
<router-link to="/">Home</router-link>
<router-link to="/add">Add Restaurant</router-link>

<a href="#" v-on:click="logout" >Logout</a>

</div>


</template>
<script>

export default 

{
    name:"HeaderPage",
    methods:{
        logout()
        {
            localStorage.clear();
            this.$router.push({name:'LoginPage'})
        }
    }
}

</script>
<style>
.nav{
    background-color: rgb(72, 72, 153);
   overflow: hidden;
}
.nav a{
     color: white;
     float: left;
     padding: 14px 16px;
     text-align: center;
     text-decoration: none;
     margin-right: 5px;
     font-size: 17px;
}
.nav a:hover{
    background: #ddd;
    color:#333;
}



</style>