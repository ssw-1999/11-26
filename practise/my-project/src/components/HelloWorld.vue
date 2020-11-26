<template>
  <div>
    <ul>
      <li>{{msg}}</li>
      <li>{{fromVue1}}</li>
    </ul>
    <new1 @getData="updateData" :prop="fromVue1"></new1>
  </div>
</template>

<script>
import new1 from './new1'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      fromVue1:''
    }
  },
  components:{
    new1
  },
  methods:{
      updateData(data){
          this.fromVue1=data;
      }
  }
  // methods:{
  //   getData:function(){
  //     this.axios.post(
  //       '/v3/acfun/crawl/content/condition',
  //       { }).then(function(res){
  //         console.log(res);
  //       })
  //   }
  // },
  // created(){
  //   this.getData();
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul li{
  list-style: none;
}
</style>
