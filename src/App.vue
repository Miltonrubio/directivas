<template>


<div>
  <h1> Directivas en VUE.js</h1>
  </div>
  <hr>

<h2> V-TEXT</h2>
<span v-text="'Hola desde vue'"></span>
<br>
<span>Hola desde vue</span>
<br>
<span v-text="titulo"></span>
<br>
<span>{{titulo}}</span>
<br>

<hr>
<h2>V-HTML</h2>

<H3 v-html="html"></H3>


<hr>
<h2>V-SHOW</h2>
<h3 >Tu edad es: {{edad}} </h3>
<h3 v-show="edad>=18">Eres mayor de edad</h3>
<h3 v-show="edad<18">Eres menor de edad</h3>

<hr>

<button @click="agreg()"> Agregar edad</button>

</template>


<script>
  export default {
   
    data:()=> ({
      titulo:"Ola desde vue.js 3",
      html:"<input type='text'> Ola!",
      edad: 14,
    }),
    methods:{
      agreg(){
        this.edad++;
      },
      quit(){
        
        this.edad--;
      }
    },
  };



</script>

<style>
div{
  text-align: center;
  margin: 0px 2rem;

}

h2{
  color:tomato;
  font-size: 2rem;
}
</style>