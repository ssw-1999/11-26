<template>
<div>
    <new6 :name='name' :age='age' :gender='gender'></new6>
</div>
</template>
<script>
import new6 from './new6'
export default {
    name:'new5',
    data(){
        return{
            name:'huahua',
            age:21,
            gender:'female'
        }
    },
    components:{
        new6
    }

}
</script>