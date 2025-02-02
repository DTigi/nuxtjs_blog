<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
      <nuxt-link class="navbar-brand" to="/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" width="30" height="30" alt="logo">
      </nuxt-link>
      <nuxt-link class="navbar-brand" to="/">
        <svg width="24" height="24" fill="none" xmlns="http://www.w3.org/2000/svg"><g clip-path="url(#avia_tab_svg__clip0_1993_871)"><path d="M17.501 19.905l-2.32-8.966 3.89-3.889a1.498 1.498 0 000-2.121 1.498 1.498 0 00-2.122 0L13.06 8.818l-8.966-2.32a1.038 1.038 0 00-1.004.27 1.051 1.051 0 00.234 1.661l6.547 3.578-3.882 3.882-2.552-.643a.508.508 0 00-.474.134l-.41.41a.501.501 0 00.092.785l2.58 1.549.41.24.206.332.22.375 1.003 1.683.354.594c.17.283.551.325.785.092l.41-.41a.495.495 0 00.134-.474l-.636-2.546L12 14.121l3.578 6.548a1.04 1.04 0 001.923-.764z" fill="#FF8E01"></path></g><defs><clipPath id="avia_tab_svg__clip0_1993_871"><path fill="#fff" d="M0 0h24v24H0z"></path></clipPath></defs></svg>
      </nuxt-link>
      <button class="navbar-toggler" type="button" data-toggle="collapse"
              data-target="#navbarSupportedContent"
              aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/">Главная</nuxt-link>
          </li>
          <li class="nav-item ">
            <nuxt-link class="nav-link" to="/contact">Контакты</nuxt-link>
          </li>
        </ul>
        <form class="form-inline my-2 my-lg-0">
          <input name="q" v-model="q" type="text" class="form-control mr-sm-2" placeholder="Поиск" aria-label="Поиск">
          <button class="btn btn-outline-success my-2 my-sm-0 mr-2" type="submit" @click.stop.prevent="submit()">Поиск</button>
        </form>
        <span class="navbar-text mr-2">Username</span>
        <nuxt-link class="btn btn-outline-light mr-2" to="/signout">Выход</nuxt-link>
        <nuxt-link class="btn btn-outline-light mr-2" to="/signin">Вход</nuxt-link>
        <nuxt-link class="btn btn-outline-light mr-2" to="/signup">Регистрация</nuxt-link>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: "Navbar",
    data(){
      return {
        q : null
      }
    },
    methods: {
      submit(){
        this.$router.push("/search?q="+this.q);
      }
    }
  }
  </script>
  
  <style scoped>
  
  </style>