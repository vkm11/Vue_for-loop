<template>
    <div>
        <h1>For loop in vue js</h1>
        <table border="1px">
            <tr>
                <td>Id</td>
                <td>Name</td>
                <td>Email</td>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.email}}</td>
            </tr>
        </table>
    </div>
    <div>
       <h1>Ex:2 For Loop in vuejs</h1>
       <ul>
           <li v-for="item in technology" :key="item">
                {{item}}
           </li>
       </ul>
       <br>
       <ul>
           <li v-for="item in user1" :key="item.email">
                Name is : {{item.name}} and Email is : {{item.email}}
           </li>
       </ul>
    </div>
</template>

<script>
export default {
   name: "Home-home",
   props: {
       data: String,
       msg: String
   },
   data(){
       return{ 
           users:[ 
               { id:1, name:'vijay', email:'vijay@gmail.com'},
               { id:2, name:'gokul', email:'gokul@gmail.com'},
               { id:3, name:'nithin', email:'nithin@gmail.com'},
               { id:4, name:'prajwal', email:'prajwal@gmail.com'},
           ],
           technology: ['html','css', 'javascript', 'reactjs', 'Angular'],
           user1: [
            {
               name: "anil",
               email: "anil@test.com"
            },
            {
               name: "sam",
               email: "sam@test.com"
            },
            {
               name: "hari",
               email: "hari@test.com"
            },
            ]  
       }
   }
}
</script>
<style scoped>
h1{
    color: orange;
}
</style>