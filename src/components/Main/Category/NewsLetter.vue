<script>
import Btn from '../../Shared/Btn.vue';

export default {
    name: 'NewsLetter',
    data() {
        return {
        }
    },
    props: {
        info: {
            type: Array,
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="newsLetter">
        <div>
            <h1>Join our newsLetter</h1>
            <p>
                Volutpat vel turpis nulla lorem sad semper. Alinquam sagittis sem libero
                viverra vehiucla nullm ut nisl.
            </p>
            <input type="text" placeholder="Insert your email ...*">
            <Btn text="Subscribe" bg=" green" color="white" />
        </div>
        <div class="croccantini">
            <img src="../../../assets/categories/food/croccantini.jpg">
        </div>
    </div>
</template>

<style lang="scss">
.newsLetter {
    width: 80%;
    margin: 0 auto;
    height: 320px;
    display: flex;
    background: linear-gradient(to bottom, #ffffff, #f5f5f5);
    margin-top: -60px;

    >div:first-child {
        width: 60%;
        padding: 40px;

        >p {
            font-size: 14px;
        }

        >* {
            line-height: 1.7;
        }

        >h1 {
            font-family: 'Mali', cursive;
        }

        input {
            width: 300px;
            padding: 8px;
            border-radius: 20px;
            border: none;
            background-color: #d8d5d5;
            margin-right: 10px;
        }
    }

    .croccantini {
        width: 60%;
        background: linear-gradient(to bottom, #ffffff, #f5f5f5);
        padding-right: 160px;

        img {
            width: 140%;
        }
    }
}
</style>