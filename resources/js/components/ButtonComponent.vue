<template>
  <button type="button" @click="emitClick" :class="color">{{ text }}</button>
</template>

<script>
export default {
    props:{
        text: {
            type:String,
            default: "",
        },
        color:{
            type: String,
            default:"",
        }
    },
    methods:{
        emitClick(){
            this.$emit('emitClick');
        }
    }
}
</script>

<style scoped>
.blue {
    background: aqua;
    border: 1px solid lightblue;
}

.red {
    background: pink;
    border: 1px solid lightblue;
}
.transparent{
    font-size: 11px;
    color: darksalmon;
    margin-left: 5px;
    vertical-align: middle;
    cursor: pointer;
    border: 1px solid lightblue;
}
</style>