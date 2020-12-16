<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
    <alert mode="primary">Firt component</alert>
    <alert mode="danger">Second component</alert>
    <alert mode="success">Third component</alert>
    

    <button-counter></button-counter>

    <br/>

    <div>
      <input type="text" v-model="lastName" placeholder="Your nice name">

      <p>
      Welcome,  {{ lastName }}
      </p>

    </div>

    <button @click="clickedMe">Click me</button>




  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data(){
    return {
      lastName: 'Perry',
      students:[
        'James',
        'John',
        'Willaim',
      ]
    }
  },

  methods:{
    clickedMe: function(){
      console.log('you clicked on the button')
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
