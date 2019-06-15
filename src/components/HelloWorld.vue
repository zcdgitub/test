<template>
  <div class="hello">

    <h2>Essential Links</h2>
 <input type="text" placeholder="请输入手机" v-model="name">
          <input type="password" placeholder="请输入密码" v-model="password">

    <ul>
      <li>
        <a
         
         @click="reg"
        >
          注册
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
       name: '',
       password: '',
    }
  },
   methods:{
      reg(){

          let $this=this;//用变量存储父函数 以便在子函数使用
         //this.$axios.post('/api/user/login',this.$qs.stringify({
         //this.$axios.post('/api/store/saveImage',this.$qs.stringify({
          //name:this.name,
          //password:this.password,
         // api_token:sessionStorage.getItem('api_token')
         //})
      this.$axios.get('http://www.lar.com/index.php/api/goods/index'
     //  this.$axios.get('http://www.lar.com/index.php/api/goodsCate/index'
       //this.$axios.get('/api/goods/detail',{params:{api_token:sessionStorage.getItem('api_token')}}
       // this.$axios.get('/api/store/saveImage',{params:{api_token:sessionStorage.getItem('api_token')}}
       //this.$axios.get('/api/store/index',{params:{api_token:sessionStorage.getItem('api_token')}}
      // this.$axios.get('/api/index/index',{params:{api_token:sessionStorage.getItem('api_token')}}
           ).then(function(response){
           console.log(response);
           // console.log(response.data.data.api_token);
          //  sessionStorage.setItem('api_token',response.data.data.api_token);
            $this.$layer.msg(response.data.msg);
         })
      }
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
