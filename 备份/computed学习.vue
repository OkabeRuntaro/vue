<template>
    <!-- html -->
     <div class="person">
         姓：<input type="text" v-model="fristname"><br>
         名：<input type="text" v-model="lastName"><br>
        姓名：<span>{{ fullName }}</span>
     </div>
</template>



<script lang="ts" setup name = 'Person'>
 
    import { ref,computed } from 'vue';


    let fristname = ref('张')
    let lastName = ref('san')

    let fullName = computed(()=>{
        return fristname.value.slice(0,1).toUpperCase() + fristname.value.slice(1) + lastName.value
    })
</script>

<style scoped>
/*样式*/
.person{
     background-color: skyblue;
}
</style>

