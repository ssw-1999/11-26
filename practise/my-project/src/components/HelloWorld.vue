<template>
  <div>
    {{msg}}
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    getData:function(){
      this.axios.post(
        '/v3/acfun/crawl/content/condition',
        { }).then(function(res){
          console.log(res);
        })
    }
  },
  created(){
    this.getData();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
