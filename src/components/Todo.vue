<template>
  <div class="todos">
    <h1>Todo App</h1>
    
    <input @keyup.enter="add" type="text" v-model="title" placeholder="What do you want to do">
    <button @click="add"> Add to list </button>

    <ul>
        <li v-for="(todo,index) in todos" v-bind:key="todo"> {{ todo }}
            <span @click="remove(index)"  class="remove">x</span>
        </li>
        <br/>
    </ul>

    </div>
</template>

<script>

export default {
  name: 'todo',
  props: {
    msg: String
  },

  data(){
      return {
          title:'',
          todos:[
              'Go to shop'
          ]
      }
  },

  methods: {
      add(){
          if(this.title !='') {
              this.todos.unshift(this.title);
              this.title =""
          }
          
      },
      remove(id) {
          this.$delete(this.todos, id)
      } 
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped lang="scss">

.remove {
    padding: .3rem .6rem;
    background-color: red;
    color: #fff;
    border-radius: 30px;
}

.remove:hover {
    cursor: pointer;
}

ui li {
    padding: .4rem;
}

</style>
