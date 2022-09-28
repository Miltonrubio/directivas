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
<h3 v-if="edad>=18 && edad >0 && edad <80 ">Eres mayor de edad</h3>
<h3 v-if="edad<18 && edad >0 && edad <80">Eres menor de edad</h3>
<h3 v-else >Edad invalida</h3>

<button @click="agreg()"> Agregar edad</button>

<button @click="quit()"> Quitar edad</button>

<hr>
<h2 >v-for</h2>

<ul >
  <li v-for="( usuario, index) in usuarios">{{index}}:{{usuario}}</li>
</ul>
<br>
<ul >
  <li v-for="(usuario, index) in usuarios" :key="index">{{index}}:{{usuario}}</li>
</ul>
<ul >
  <li v-for="(valor, clave) in ususarioss" :key="clave">{{clave}}:{{valor}}</li>
</ul>
<hr>
<h1>Empleando V-on</h1>
<div @dblclick="click()" class="contenedor"> Clicks: {{clicks}}

</div>

</template>

<script>
  export default {
   
    data:()=> ({
      titulo:"Ola desde vue.js 3",
      html:"<input type='text'> Ola!",
      edad: 5,
      usuarios: ["Melissa", "Fernando","Raul", "José"],
      ususarioss:{nombre: "juana de arco"},
      clicks: 0,

    }),
    methods:{
      agreg(){
        this.edad++;
      },
      quit(){
        
        this.edad--;
      },
      click(){
this.clicks++
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
.contenedor{
        background: pink;
        color: snow;
        font-weight: bolder;
        height: 400px;
}
</style>