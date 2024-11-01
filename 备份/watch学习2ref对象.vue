<template>
    <!-- html -->   

<span>姓名：{{ person.name }}</span><br>
<span>年龄：{{ person.age }}</span><br>
<button @click="chengeName">修改名字</button>
<button @click="chengeAge">修改年龄</button>
<button @click="chengePerson">修改人</button>

</template>



<script lang="ts" setup name = 'Person'>
    import {ref,watch} from 'vue'

    let person = ref({
        name :"张三",
        age : 18
    })

    function chengeName(){
        person.value.name += '~'
    }
    function chengeAge(){
        person.value.age += 1
    }
    function chengePerson(){
        person.value = {name:'李四',age:20}
    }
    //监视
    watch(person,(newValue,oldValue)=>{
        console.log(newValue,oldValue)
    },{deep:true,immediate:true})
</script>

<style scoped>
/*样式*/
.person{
     background-color: skyblue;
}
</style>

