<template>
  <div>
    {{msg}}
    {{fromnew2}}
    <new4/>
  </div>
</template>

<script>
import new4 from './new4'
import {EventBus} from './event-bus'
export default {
  name: 'new3',
  data () {
    return {
      msg: 'Welcome to new3',
      fromnew2:''
    }
  },
  components:{
    new4
  },
  beforeMount(){
      EventBus.$on('action',key => {
          this.fromnew2=key.msg;
      })
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
