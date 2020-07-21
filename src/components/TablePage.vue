<template>
    <div>
        
        <table>
            <tr>
                <th v-for="(value,key) in heder" :key="key">
                    {{value.name}}
                </th>
            </tr>
           <tr v-for="(value,key) in result" :key="key">
               <td>{{ value.name}}</td>
               <td>{{ value.lastname}}</td>
               <td>{{ value.mobile}}</td>
           </tr>
          
        </table>
    </div>
</template>
<script>
export default {
    name: "table-page",
    props: {
        heder:{
            type:Array
        },
        result:{
            type:Array
        }
    }
    
}
</script>
<style>
 table
{
    width: 100%;
      border-spacing: 15px;

}

    table,th,tr,td {
       
        border: 1px solid black;
        padding: 5px; 

    }
    
   

</style>