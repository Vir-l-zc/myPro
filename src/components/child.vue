<template>
    <div>
        子组件接收到的数据是{{parentUsername}}
        <button @click="sendDataToParent">向父组件传递数据</button>
        
    </div>
</template>

<script>
    export default {
            props:['parentUsername'],
            components: {

        },
        data(){
            return {
                number:90
            }
        },
        methods: {
    sendDataToParent(){
        this.$emit('parentReceiveNumber',this.number)
    }
        }
    }
</script>

<style lang="scss">

</style>