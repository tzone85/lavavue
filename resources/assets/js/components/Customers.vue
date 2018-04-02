<template>
   <table class="table table-bordered table-striped table-condensed">
      <thead>
         <tr>
            <th>Name</th>
            <th>Email</th>
         </tr>
      </thead>
   </table>
</template>

<script>
    export default {
        data(){
            return{
                customers: [
                    {name: 'Mncedi Mini', email:'mncedi@thandotec.co.za'},

                    {name: 'Noncedo Mini', email:'noncedo@thandotec.co.za'}
                ],
            }
        }
    }
</script>