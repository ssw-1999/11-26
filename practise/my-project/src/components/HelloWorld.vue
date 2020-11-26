<template>
  <div>
    <ul>
      <li>{{msg}}</li>
      <li>{{fromVue1}}</li>
      <li>{{son1}}</li>
    </ul>
    <new1 @getData="updateData" :prop="fromVue1" ref="new1"></new1>
    <new3 ref="new3"></new3>
  </div>
</template>

<script>
import new1 from './new1'
import new3 from './new3'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      fromVue1:'',
      son1:''
    }
  },
  components:{
    new1,
    new3
  },
  provide:{
    hello:'hahaha'
  },
  // computed:{
  //     son1(){
  //       console.log(this.$children);
  //       return this.$children[0].son;
  //     }
  // },
  methods:{
      updateData(data){
          this.son1=this.$children[0].son;
          this.fromVue1=data;
      }
  },
  created(){
    // console.log(this.$children);
    // console.log(this.$refs.new3.msg)
  },
  beforeMount(){
    // console.log(this.$children);
    // console.log(this.$refs.new3.msg)
  },
  mounted(){
    // console.log(this.$children);
    console.log(this.$refs.new3.msg)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul,li{
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>
