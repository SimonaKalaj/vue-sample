<template>
<div>
    <table>
            <tr>
                <th v-for="(value,key) in heder" :key="key">
                    {{value.last}}
                </th>
            </tr>
           <tr v-for="(value,key) in result" :key="key">
               <td>{{ value.name}}</td>
               <td>{{ value.last}}</td>
           </tr>
    </table>
</div>
    
</template>
<script>
export default {
    name: "table-two",
    data() {
        return {
           heder:[
               {
                    last: "NAME"
               },
               {
                    last: "LAST"
               }
            ],
            result:[
               {
                     name: "Simona",
                    last: "Kalaj"
               },
               {
                    name: "Sofi",
                    last: "Kalaj"
               }
            
            ] 
        } 
        

    }
}
</script>
<style>

</style>