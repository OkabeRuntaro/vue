<template>
    <!-- html -->   

<span>姓名：{{ person.name }}</span><br>
<span>年龄：{{ person.age }}</span><br>
<button @click="chengeName">修改名字</button>
<button @click="chengeAge">修改年龄</button>
<button @click="chengePerson">修改人</button>

</template>



<script lang="ts" setup name = 'Person'>
    import {reactive,watch} from 'vue'

    let person = reactive({
        name :"张三",
        age : 18
    })

    function chengeName(){
        person.name += '~'
    }
    function chengeAge(){
        person.age += 1
    }
    function chengePerson(){
        Object.assign(person , {name:'李四',age:20})
    
    }
    // //监视,reacative对象默认深度监视，无法关闭
     watch(person,(newValue,oldValue)=>{
        console.log(newValue,oldValue)
    })
</script>

<style scoped>
/*样式*/
.person{
     background-color: skyblue;
}
</style>

