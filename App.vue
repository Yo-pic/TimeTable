<template>
  <div id="app">
<h1>時間割</h1>


    <table id ="table1">
  <tr>
    <th>月曜日</th><th>火曜日</th><th>水曜日</th><th>木曜日</th><th>金曜日</th>
  </tr>
</table>


    <table id="table">
        <tr>
          <td><p>{{classes[0]}}</p></td><td><p>{{classes[5]}}</p></td><td><p>{{classes[10]}}</p></td><td><p>{{classes[15]}}</p></td>
          <td><p>{{classes[20]}}</p></td>
        </tr>
        <tr>
          <td>{{classes[1]}}</td><td>{{classes[6]}}</td><td>{{classes[11]}}</td><td>{{classes[16]}}</td><td>{{classes[21]}}</td>
        </tr>
        <tr>
          <td>{{classes[2]}}</td><td>{{classes[7]}}</td><td>{{classes[12]}}</td><td>{{classes[17]}}</td><td>{{classes[22]}}</td>
        </tr>
        <tr>
          <td>{{classes[3]}}</td><td>{{classes[8]}}</td><td>{{classes[13]}}</td><td>{{classes[18]}}</td><td>{{classes[23]}}</td>
        </tr>
        <tr>
          <td>{{classes[4]}}</td><td>{{classes[9]}}</td><td>{{classes[14]}}</td><td>{{classes[19]}}</td><td>{{classes[24]}}</td>
        </tr>

      <tr>
        <td></td><td></td><td></td><td></td><td></td>
      </tr>

      </table>

    <select v-model = "selected">
    <option disabled value = "">時限選択</option>
    <option>月, 1・2限</option><option>月, 3・4限</option><option>月, 5・6限</option><option>月, 7・8限</option><option>月, 9・10限</option>
      <option>火, 1・2限</option><option>火, 3・4限</option><option>火, 5・6限</option><option>火, 7・8限</option><option>火, 9・10限</option>
      <option>水, 1・2限</option><option>水, 3・4限</option><option>水, 5・6限</option><option>水, 7・8限</option><option>水, 9・10限</option>
      <option>木, 1・2限</option><option>木, 3・4限</option><option>木, 5・6限</option><option>木, 7・8限</option><option>木, 9・10限</option>
      <option>金, 1・2限</option><option>金, 3・4限</option><option>金, 5・6限</option><option>金, 7・8限</option><option>金, 9・10限</option>

    </select>
    <input v-model="input" @keydown.enter="addTimetable" />
    <button @click="addTimetable">add</button>


    </div>




</template>

<script>



export default {
  name: 'App',
  data(){
    return{
      input: "",
      selected: "",
      classes:[],


    };
  },

  methods:{
    addTimetable() {
      if(this.selected === '月, 1・2限') {

        this.classes[0]=this.input;

      }

      else if(this.selected === '月, 3・4限'){
        this.classes[1]= this.input;
      }

      else if(this.selected === '月, 5・6限'){
        this.classes[2]= this.input;
      }

      else if(this.selected === '月, 7・8限'){
        this.classes[3]= this.input;
      }

      else if(this.selected === '月, 9・10限'){
        this.classes[4]= this.input;
      }

      else if(this.selected ==='火, 1・2限'){
        this.classes[5]= this.input;
      }

      else if(this.selected === '火, 3・4限'){
        this.classes[6]= this.input;
      }

      else if(this.selected ==='火, 5・6限' ){
        this.classes[7]= this.input;
      }

      else if(this.selected === '火, 7・8限'){
        this.classes[8]= this.input;
      }

      else if(this.selected ==='火, 9・10限' ){
        this.classes[9]= this.input;
      }

      else if(this.selected === '水, 1・2限'){
        this.classes[10]= this.input;
      }

      else if(this.selected === '水, 3・4限'){
        this.classes[11]= this.input;
      }

      else if(this.selected === '水, 5・6限'){
        this.classes[12]= this.input;
      }

      else if(this.selected === '水, 7・8限'){
        this.classes[13]= this.input;
      }

      else if(this.selected === '水, 9・10限'){
        this.classes[14]= this.input;
      }

      else if(this.selected === '木, 1・2限'){
        this.classes[15]= this.input;
      }

      else if(this.selected === '木, 3・4限'){
        this.classes[16]= this.input;
      }

      else if(this.selected === '木, 5・6限'){
        this.classes[17]= this.input;
      }

      else if(this.selected === '木, 7・8限'){
        this.classes[18]= this.input;
      }

      else if(this.selected === '木, 9・10限'){
        this.classes[19]= this.input;
      }

      else if(this.selected === '金, 1・2限'){
        this.classes[20]= this.input;
      }

      else if(this.selected === '金, 3・4限'){
        this.classes[21]= this.input;
      }

      else if(this.selected === '金, 5・6限'){
        this.classes[22]= this.input;
      }

      else if(this.selected === '金, 7・8限'){
        this.classes[23]= this.input;
      }

      else if(this.selected === '金, 9・10限'){
        this.classes[24]= this.input;
      }

      this.input = "";
    },

  },
};

</script>

<style>
td{
  text-align: center;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#table {

  margin:0 auto;
  border-collapse: collapse;
  border: 3px solid #ccc;

}

#table td {

  border:1px solid #ccc;
  height: 60px;
  width: 190px;
  text-align: center;
  vertical-align: middle;
  font-size: 17px;
  cursor: pointer;

}

#table1{
  margin:0 auto;
  border-collapse: collapse;
  border: 3px solid #ccc;
}
#table1 th{

  border:1px solid #ccc;
  height: 60px;
  width: 190px;
  text-align: center;
  vertical-align: middle;
  font-size: 30px;
  cursor: pointer;

}




</style>
