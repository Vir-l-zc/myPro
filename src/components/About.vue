<template>
    <div id="abc">
{{message}}
    </div>
</template>

<script>
    export default {
        data(){
            return {
               message:'我是About' 
            }
        },
    }
</script>

<style>
#abc{
    color: blueviolet;
    font-size: 20px;
}
</style>