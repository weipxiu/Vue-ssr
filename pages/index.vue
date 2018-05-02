<template>
  <section class="container">
    欢迎来到nuxt.js世界！
    <h1 class="title">
      USERS
    </h1>
    <nuxt-link to="/0">user-link</nuxt-link>
    <input type="text" v-model="abc">
    <button @click="onbutton">按钮</button>
  </section>
</template>

<script>
import axios from '~/plugins/axios'
export default {
  data(){
    return {
      abc:''
    }
  },
  methods:{
    onbutton(){
      this.$router.push('/' + this.abc)
    }
  }
}
</script>

<style scoped>
.title
{
  margin: 30px 0;
}
.users
{
  list-style: none;
  margin: 0;
  padding: 0;
}
.user
{
  margin: 10px 0;
}
</style>
