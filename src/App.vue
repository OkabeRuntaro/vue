<template>
    <!-- html -->
     <div class="app">
        <h1>你哈</h1>
        <Person></Person>
     </div>
</template>

<script lang="ts" setup name="App">
//JS/TS
    import Person from './components/Person.vue';
    // export default{
    // name:"App",  //组件名字
    // components:{Person}
    // }
</script>

<style>
/*样式*/
.app{
     background-color: bisque;
}
</style>

