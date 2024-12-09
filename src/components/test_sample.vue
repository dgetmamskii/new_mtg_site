<template>
    <input type="text" v-model="name" placeholder="Имя">
    <input type='password' v-model="password" placeholder="Пароль">
    <button @click="sendData()">Отправить</button>
  
    <p className="error">{{ error }}</p>
    <Menu v-for="(el, index) in this.users" :key="index" :element="el" :index="index" :deleteElem="deleteElem"/>
  </template>
  
  <script>
  import Menu from './components/up_menu.vue'
  
  export default {
    components : { Menu },
    data() {
      return {
        users : [],
        error : "",
        name : "",
        password : ""
      }
    },
    methods: {
      sendData() {
        if (this.name == ''){
          return this.error = "Имя не введено"
        }
        this.users.push({
          name : this.name,
          password : this.password
        })
      },
      deleteElem(index) {
        this.users.push({name : index})
      }
    }
  }
  </script>
  
  <style scoped>
  h3 {
    font-size: larger;
  }
  
  p {
    color: rgb(145, 0, 0);
  }
  
  .menu {
    color: rgb(145, 0, 0);
  }
  
  .header {
    text-align: center;
    
  }
  </style>
  