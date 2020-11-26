<template>
  <div>
      <ul>
          <li>{{msg}}</li>
          <li>{{key}}</li>
      </ul>
    <button @click="n2ton4">new2send</button>
  </div>
</template>

<script>
import {EventBus} from './event-bus'
export default {
  name: 'new2',
  data () {
    return {
      msg: 'Welcome to new2',
      word2:'',
    }
  },
  inject:['hello'],
  computed:{
      key(){
        return this.hello;
      }
  },
  created(){
      console.log(this.hello);
  },
  methods:{
      n2ton4(){
          EventBus.$emit('action',{
              msg:this.hello
          })
      }
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
