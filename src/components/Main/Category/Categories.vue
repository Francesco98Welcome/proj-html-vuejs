<script>
export default {
    name: 'Category',
    data() {
        return {
        }
    },
    props: {
        info: {
            type: Array,
        }
    },
}
</script>

<template>
    <div class="category">
        <div v-for="info in info">
            <div>
                <img :src='info.img' />
            </div>
            <div>
                {{ info.text }}
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.category {
    // border: 1px solid black;
    display: flex;

    justify-content: space-between;

    >div {
        // border: 1px solid black;
        width: calc(100% / 4);
        margin: 0 auto;
        margin: 6px;
        text-align: center;

        img {
            width: 100%;
            margin-bottom: 15px;
        }
    }
}
</style>