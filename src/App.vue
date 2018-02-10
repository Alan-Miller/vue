<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Todos</h1>
    <input type="text" v-model='inputText'>
    <button @click='addTodo'>Add Todo</button>

    <p v-for='(friend, i) in friends' :key='i'>{{friend}}</p>
    <p v-for='(todo, i) in todos' :key='i'>{{todo}}
      <button @click='() => deleteTodo(i)'></button>
    </p>

    <form @submit.prevent='submitForm'>
      <input type="text" v-bind:value='message' v-on:input='handleChange'>
    </form>
    <div @keyup.enter='somemethod'></div>

    <header @changeName='nameIsChanging' :myName='myName'></header>
    
    <p>{{message}}</p>
    <img :src="image" alt="">
    <HelloWorld/>


  </div>

</template>

<script>
import HelloWorld from './components/HelloWorld'
import JoeHeader from './components/Header'

export default {
  // name: 'App',
  // components: {
  //   HelloWorld
  // }
  data() {
    return {
      message: "input text",
      image: "https://cdn.vox-cdn.com/thumbor/Wd-2zsFlWxXz1HgmGEEwXx5iYBI=/0x0:1000x605/1200x800/filters:focal(420x223:580x383)/cdn.vox-cdn.com/uploads/chorus_image/image/48780381/duck.0.png",
      friends: ['Harry', 'Nancy', 'Jimbo'],
      todos: [],
      inputText: '',
      myName: "Joe"
    }
  },
  methods: {
    handleChange(e) {
      this.message = e.target.value
    },
    addTodo() {
      this.todos.push(this.inputText)
      this.inputText = ''
    },
    deleteTodo(index) {
      this.todos.splice(index, 1)
    },
    nameIsChanging(data) {
      console.log(data)
      this.myName = data
    }
  },
  components: {
    "header": JoeHeader
  }
}
</script>

<style scoped> 
/* <style scoped lang='scss'> 
This scopes the styles to this component 
This uses the given preprocessor
*/
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/* This is a single-file component. It has the template, the script, and the style/CSS. */
</style>
