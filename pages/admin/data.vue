<template>
    <div class="bg-gray-900 p-3 min-h-screen text-white">

        <button class="rounded border px-4 py-2 m-2" @click="details">Refresh Again </button>

        <table class="w-full">
            <tr>
                <th>Name</th>
                <th>Number</th>
                <th>Date of Appointment</th>
                <th>Posted on</th>
                <th>Action</th>
            </tr>
            <tr v-for="d in data" :key="d.uuid">
                <td> {{ d.name }} </td>
                <td>  {{ d.mobile_no }} </td>
                <td>  {{ d.date }} </td>
                <td> {{ d.__createdtime__ }}</td>
                <td> <button @click="deletes(d.uuid)"> Delete </button> </td>
            </tr>
        </table>        
    </div>
</template>

<script>
export default {
    data() {
        return {
          data : {}
        }
    },
    mounted () {
        this.details()
    },


    methods: {
        async details() {          
            let headersList = {
            "Authorization": "Basic bWFsd2FyZW1hbnU6TWFudUBoYXJwZXIx",
            "Content-Type": "application/json"
            }

            let bodyContent = JSON.stringify({
                "operation": "sql",
                "sql": "select * from anju.appointments"            
            });

            let response = await fetch("https://po-manu.harperdbcloud.com", { 
                method: "POST",
                body: bodyContent,
                headers: headersList
            });

            let data = await response.json();
            console.log(data);                            
            this.data = data
        },

        async deletes(x) {          
            let headersList = {
            "Authorization": "Basic bWFsd2FyZW1hbnU6TWFudUBoYXJwZXIx",
            "Content-Type": "application/json"
            }

            let bodyContent = JSON.stringify({
                "operation": "delete",
                "table": "appointments",
                "schema": "anju",
                "hash_values": [ x ] 
            });

            let response = await fetch("https://po-manu.harperdbcloud.com", { 
                method: "POST",
                body: bodyContent,
                headers: headersList
            });

            let data = await response.json();
            console.log(data);                            
            alert(data.message)
            this.details()
        },
    },
}
</script>


<style>
th, td {
    border: 1px solid gray;
    padding: 5px;
}
</style>