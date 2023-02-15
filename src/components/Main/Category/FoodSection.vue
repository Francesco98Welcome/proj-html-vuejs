<script>
// immagini per la sezione del cibo, la seconda sezione del main.
import kibble from "../../../assets/categories/food/kibble210x200.png";
import moist from "../../../assets/categories/food/moist210x200.png";
import frozen from "../../../assets/categories/food/frozen200x210.png";

import Btn from '../../Shared/Btn.vue';

export default {
    name: 'FoodSection',
    data() {
        return {
            info: [
                { text: 'Kibble', desc: 'Dry dog food', img: kibble, btnText: 'Shop dry food' },
                { text: 'Moist', desc: 'Canned dog food', img: moist, btnText: 'Shop moist food' },
                { text: 'Frozen', desc: 'Freeze-Dried dog food', img: frozen, btnText: 'Shop frozen food' }
            ],
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="foodSection">
        <div v-for="info in info">
            <div>
                <h3>{{ info.text }}</h3>
                <p>{{ info.desc }}</p>
                <img :src='info.img' />
                <Btn :text="info.btnText" bg=" #3d6f42" color="white" />
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.foodSection {
    min-height: 470px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;

    >div {
        width: 32.5%;
        position: relative;
        border: 1px solid black;
        background-color: $color_dark-green;

        >div {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;

            >h3 {
                margin-bottom: 12px;
                color: white;
            }

            >p {
                color: #569a60;
            }
        }

    }

}
</style>