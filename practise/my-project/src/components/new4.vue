<template>
  <div>
    {{msg}}
    {{fromnew2}}
  </div>
</template>

<script>
import EventBus from './event-bus'
export default {
  name: 'new4',
  data () {
    return {
      msg: 'Welcome to new4',
      fromnew2:''
    }
  },
  beforeMount(){
      EventBus.$on('action',key => {
          this.fromnew2=key;
      })
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
