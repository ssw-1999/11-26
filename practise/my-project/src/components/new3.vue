<template>
  <div>
    {{msg}}
    <new4/>
  </div>
</template>

<script>
import new4 from './new4'
export default {
  name: 'new3',
  data () {
    return {
      msg: 'Welcome to new3'
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
