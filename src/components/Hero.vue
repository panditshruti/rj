<template>
    <div class=" w-full h-full">

      <!-- <Child name="shruti" /> -->
     
        <input type="text" v-model="name"/>
        <h1>{{name}}</h1>
        <h1>{{name.length}}</h1>
        <div class="w-40 h-40 bg-blue-800 mx-5" v-if="funsk">dsfgdfgsdf</div>
        <Button @click="show" class="bg-red-500">clicked this</Button>
        <h1>{{email}}</h1>
        <h1>{{mobbile}}</h1>
        <h1>{{mobbile=88888}}</h1>
        <h1> Name{{getname("shrutitiot")}}</h1>  

        <h1>{{green}}Shruti</h1>

        
<!-- 9th videios -->

    <button v-on:click="getData('buttion 1 clicked')" >button 1</button>
    <button v-on:dblclick="getData('buttion double clicked')" >button 2</button>
    <h1 v-on:mousemove="getConsole()">Home Componnet</h1>
      

    <!-- 11 th video -->

    <br /> 
    <br/>

    <h1> Get Input field value</h1>
    <input type="text" placeholder="Enter Email" v-model="emailss" />
    <br />
    <br/>
    <input type="Password" placeholder="Enter Password" v-model="Password" />
    <br />
    <br/>
    <button v-on:click="getDetails()" type="button">Get Value</button>
    <br />
    <br/>
  <!-- 12 th video -->

  <h1> Get chechBox & Radio Button Value</h1>
  <h3>Technalogy</h3>
  <br />
    <br/>
  <label for="java">java</label>
  <input type="checkbox" value="java" v-model="technalogy" id="java">
  <br />
    <br/>

    <label for="java">Kotlin</label>
  <input type="checkbox" value="Kotlin" v-model="technalogy" id="Kotlin">

  <br />
    <br/>

    <label for="java">phython</label>
  <input type="checkbox" value="phython" v-model="technalogy" id="phython">


<h1>Foor loop in vue js</h1>

<ul>
  <li v-for="item in technalogy" :key=" item">
  {{ item }}
  </li>
</ul>

<br />
<br />

<ul >
  <li v-for="item in user" :key="item.email">
    name is :{{ item.name }} and email is :{{ item.email }}
  </li>
</ul>

<br />
<br />

<h1>{{text}}</h1>
<div v-html="tag">
</div>


<div class="h-screen w-full bg-red-700" >




</div>


    </div>
  </template>

<script>
// import Child from './Child.vue'
export default {
  // name:Hero,
  // components:{
  //   Child
  // }
data(){
    return {
        name:"",
        namess:"",
        inputs:"",
        funsk:true,
        email:'shruti@.com',
        mobbile:77777,

        email:null,
        Password:null,

        text:"Shruti pandit",
        tag:"<h1> sk pandit</h1>",

        technalogy:['java','phy','node'],
        user:[{
          name:"Anil",
          email:'aniltest.com'
        },
        {

          name:"sam",
          email:'anssasdfiltest.com'
                  }   ,
      
      ],
        getname:function(a){
        return a;
        },

    

  
    }
},


methods:{
    show(){
        this.funsk=!this.funsk
    },

    getData(data){
        alert(data);
    },
    getConsole(){
        console.warn("funtion callled")
    },
    getDetails(){
        console.warn("values :",this.email,this.Password)

    }
  }
}

</script>

