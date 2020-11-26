<template>
  <div>
    {{msg}}
    {{key}}
  </div>
</template>

<script>
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
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
