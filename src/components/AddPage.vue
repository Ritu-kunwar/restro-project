<template>


<HeaderPage /> 
<h1>Welcome to Add Restaurant Page</h1>
<form class="add">
    <input type="text" name="name" placeholder="Enter Name" v-model="restaurant.name" />
    <input type="text" name="address" placeholder="Enter Address" v-model="restaurant.address" />
    <input type="text" name="contact" placeholder="Enter Conact" v-model="restaurant.contact" />
    <button type="button" v-on:click="addRestaurant">Add new Restaurant</button>
</form>
</template>
<script>
import HeaderPage from './HeaderPage.vue';
import axios from 'axios';

export default {
    name:'AddPage',
    components:{
        HeaderPage
    },
    data(){
        return {
            restaurant :{
                name:'',
                address: '',
                contact: '',
            
            }
        }
    },
    methods:{
      async  addRestaurant()
        {
            console.warn(this.restaurant)
            const result = await  axios.post(" http://localhost:3000/restaurant",
            {
                name:this.restaurant.name,
                address:this.restaurant.address,
                contact:this.restaurant.contact,
            });
            if(result.status==201){
                this.$router.push({name:'HomePage'})
            }
          console.warn("result",result)  
        }

    },
    mounted()
    {
        let user= localStorage.getItem('user-info');
        if(!user)
        {
             this.$router.push({name:"SignUp"})   
        }

    }
}
</script>