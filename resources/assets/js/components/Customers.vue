<template>
   <table class="table table-bordered table-striped table-condensed">
      <thead>
         <tr>
            <th>Name</th>
            <th>Email</th>
         </tr>
      </thead>

       <tbody>
        <tr v-for="customer in customers">

            <td>{{ customer.name }}</td>
            <td>{{ customer.email }}</td>

        </tr>
       </tbody>
   </table>
</template>

<script>
    export default {
        data(){
            return{
                customers: [

                    /*{name: 'Mncedi Mini', email:'mncedi@thandotec.co.za'},
                    {name: 'Noncedo Mini', email:'noncedo@thandotec.co.za'}*/

//                    going to be reading from db now

                ],
            }
        },

        create(){
            this.fetchCustomer();
        },

        methods:{
            fetchCustomer(){
                this.$http.get("customer").then(response => {this.customers = response.data.customers});
            }
        }
    }
</script>