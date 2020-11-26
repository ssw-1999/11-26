<template>
  <div>
      <ul>
          <li>{{msg}}</li>
          <li>
              <input type="text" v-model="word1">
              <button @click="sendData()">像父组件发送数据</button>
          </li>
          <li>{{prop}}</li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'new1',
  data () {
    return {
      msg: 'Welcome to new1',
      word1:""
    }
  },
  props:{
      prop:String
  },
  methods:{
      sendData(){
          this.$emit('getData',this.word1)
      }
  }
//   methods:{
//     getData:function(){
//       this.axios.post(
//         '/v3/acfun/crawl/content/condition',
//         { }).then(function(res){
//           console.log(res);
//         })
//     }
//   },
//   created(){
//     this.getData();
//   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul li{
  list-style: none;
}
</style>
