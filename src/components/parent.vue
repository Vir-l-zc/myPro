<template>
    <div>
    <p>父组件的数据是{{msg}}</p>
    <Child :parentUsername="msg" @parentReceiveNumber="handle"></Child>
    接收到子组件的值为{{values}}
    </div>
</template>

<script>
import Child from './child.vue'
    export default {
        props: {

        },
        components: {
        Child
        },
        data(){
            return {
                msg:"hello",
                values:''
            }
        },
        methods: {
    handle(value){
        console.log('接收到了子组件的数据'+value);
         this.values=value
    }
        }
    }
</script>

<style>

</style>