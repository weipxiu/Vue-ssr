<template>
  <section class="container">
    <img src="~assets/img/logo.png" alt="Nuxt.js Logo" class="logo" />
    <h1 class="title">
      这就是一个公共的页面，假设如此！
    </h1>
    <h2>
      当前你访问的路由为{{$route.params.id}}
    </h2>
    <!-- <h2 class="info">
      {{ user.name }}
    </h2> -->
    <nuxt-link class="button" to="/">
      Users
    </nuxt-link>
  </section>
</template>

<script>
import axios from '~/plugins/axios'

export default {
  validate({params}){
    console.log(params.id)
    return params.id == 1
    //路由参数判断不能使用===，因为拿到的是字符串
  }
  // ,
  // name: 'id',
  // asyncData ({ params, error }) {
  //   return axios.get('/api/users/' + params.id)
  //     .then((res) => {
  //       return { user: res.data }
  //     })
  //     .catch((e) => {
  //       error({ statusCode: 404, message: 'User 没找到' })
  //     })
  // },
  // head () {
  //   return {
  //     title: `User: ${this.user.name}`
  //   }
  // }
}
</script>

<style scoped>
.title
{
  margin-top: 30px;
}
.info
{
  font-weight: 300;
  color: #9aabb1;
  margin: 0;
  margin-top: 10px;
}
.button
{
  margin-top: 30px;
}
</style>
