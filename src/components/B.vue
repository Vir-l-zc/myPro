<template>
    <div id="bb">
组件B组件了组件A传递过来的数据{{ msgFromA }}
    </div>
</template>

<script>
import bus from '../eventBus.js'
    export default {
        props: {

        },
        components: {

        },
        data(){
            return {
                msgFromA:''
            }
        },
        created() {
            bus.$on('share',(value)=>{
                this.msgFromA=value
            })
        },
        methods: {

        }
    }
</script>

<style>
#bb{
    color: cornflowerblue;
    font-size: 40px;
}
</style>