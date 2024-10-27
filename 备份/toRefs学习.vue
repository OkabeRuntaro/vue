<template>
    <!-- html -->
     <div class="person">
         <h2>姓名：{{ person.name }}</h2>
         <h2>年龄：{{ person.age }}</h2>
         <button @click="chengeName">修改名字</button>
         <button @click="chengeAge">修改年龄</button>
     </div>
</template>



<script lang="ts" setup name = 'Person'>
    import {reactive, ref,toRefs} from 'vue';

    let person = reactive({
        name : '张三',
        age :18
    })
    //toRefs学习
    let {name,age} = toRefs(person)

    function chengeName(){
        person.name += '~'
    }
    function chengeAge(){
        person.age += 1
    }

</script>

<style scoped>
/*样式*/
.person{
     background-color: skyblue;
}
</style>

