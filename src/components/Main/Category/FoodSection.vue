<script>
export default {
    name: 'FoodSection',
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
    <div class="foodSection">
        <div v-for="info in info">
            <div>
                <h3>{{ info.text }}</h3>
                <p>{{ info.desc }}</p>
                <img :src='info.img' />
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.foodSection {
    border: 1px solid black;
    min-height: 470px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;

    >div {
        border: 1px solid black;
        width: 32.5%;
        position: relative;

        >div {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;

            >h3 {
                margin-bottom: 12px;
            }
        }

    }

}
</style>