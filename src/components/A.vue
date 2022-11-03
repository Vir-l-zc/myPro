<template>
    <div id="aa">
<button @click="sendMsg">向兄弟组件B传递数据</button>
    </div>
</template>

<script>
import bus from '../eventBus.js'
    export default {
        props: [],
        components: {

        },
        data(){
            return {
                msg:'你好帅哥'
            }
        },
        methods: {
    sendMsg(){
        bus.$emit('share',this.msg)
    }
        }
    }
</script>

<style>
#aa{
    width: 200px;
    height: 100px;
    background-color: green;
    font-size: 30px;
}
</style>