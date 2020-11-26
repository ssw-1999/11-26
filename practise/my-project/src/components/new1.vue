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
      <new2/>
  </div>
</template>

<script>
import new2 from './new2'
export default {
  name: 'new1',
  data () {
    return {
      msg: 'Welcome to new1',
      word1:"",
      son:"son1"
    }
  },
  components:{
      new2
  },
  props:{
      prop:String
  },
  methods:{
      sendData(){
          console.log(this.$parent.msg)
          this.$emit('getData',this.word1)
          this.word1="";
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
  margin: 0;
  padding: 0;
}
</style>
