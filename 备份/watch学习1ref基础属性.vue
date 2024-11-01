<template>
    <!-- html -->

<span>{{ sum }}</span>
<button @click="chengeSum">+1</button>
</template>



<script lang="ts" setup name = 'Person'>
    import {ref,watch} from 'vue'

    let sum = ref(0)

    function chengeSum(){
        sum.value += 1
    }

    const stopWatch = watch(sum,(NewSum,OldSum)=>{
        console.log("sum变化了",NewSum,OldSum)
        if(sum.value>10){
            stopWatch();
        }
    })

</script>

<style scoped>
/*样式*/
.person{
     background-color: skyblue;
}
</style>

