<template>
<div>
    <new7 v-bind="$attrs"></new7>
    <div>{{msg}}</div>
</div>
</template>
<script>
import new7 from './new7'
export default {
    name:'new6',
    data(){
        return{
            msg:this.name
        }
    },
    props:{
        name:String,
    },
    // computed:{
    //     msg(){
    //         return this.name
    //     }
    // },
    components:{
        new7
    },
    created(){
        console.log(this.name,this.$attrs);
    },
    

}
</script>