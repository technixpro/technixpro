<template>
  <div id="app">

  <table>
    <thead>
      <tr>
        <th>Metric</th>
        <th  v-for="dt in muniData">{{ dt.dateOf }}</th>
        <th>Actions</th>
      </tr>
    </thead>
    <tbody>
        <tr>
          <td>AV</td>
          <template v-for="val in muniData">      
            <td v-for="value in val.values">{{ value.assessed_value }}</td>           
          </template>
            <td>
              <button>Add</button>
              <button>Edit</button>
              <button>Delete</button>
            </td> 
        </tr>
        <tr>
          <td>FV</td>
          <template v-for="val in muniData">      
            <td v-for="value in val.values">{{ value.full_value }}</td>           
          </template>
            <td>
              <button>Add</button>
              <button>Edit</button>
              <button>Delete</button>
            </td> 
        </tr>
    </tbody>
  </table>


  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  data(){
    return {
            muniData: [
            {
              dateOf: "12/31/2012",
              values: [
                {
                  assessed_value: 819.06,
                  full_value: 157.68,
                  top_ten_taxpayers: 4.31
                }
              ]
            },
            {
              dateOf: "12/31/2013",
              values: [
                {
                  assessed_value: 819.06,
                  full_value: 157.68,
                  top_ten_taxpayers: 4.31
                }
              ]
            },
            {
              dateOf: "12/31/2014",
              values: [
                {
                  assessed_value: 819.06,
                  full_value: 157.68,
                  top_ten_taxpayers: 4.31
                }
              ]
            }
          ]
    } 
    
  } 
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
