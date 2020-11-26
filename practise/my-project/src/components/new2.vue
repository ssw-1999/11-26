<template>
  <div>
    {{msg}}
    {{msg}}
  </div>
</template>

<script>
export default {
  name: 'new2',
  data () {
    return {
      msg: 'Welcome to new2'
    }
  },
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

</style>
