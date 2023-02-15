<script>
export default {
    name: 'Btn',
    data() {
        return {
        }
    },

    props: {
        text: {
            type: String,
            //default: ''
        },
        bg: {
            type: String,
            //default: 'gray'
        },
        color: {
            type: String,
            //default: 'black'
        }
    }
}
</script>

<template>
    <button :style="{ backgroundColor: bg, color: color, width: width }">{{ text }}</button>
</template>

<style lang="scss">
button {
    border-radius: 20px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 22px;
    padding-right: 22px;
    border: none;
}
</style>