<script>
import dog from "../../../assets/categories/animals/dogball.jpg";
import cat from "../../../assets/categories/animals/catwhite.jpg";

import Btn from '../../Shared/Btn.vue';
export default {
    name: 'AccessoryArrival',
    data() {
        return {
            info: [
                { text: 'find the best animal supplies', desc: 'popular accessories', btnText: 'View all toys accessories', img: dog },
                { text: 'find the best food', desc: 'new food arrival', btnText: 'View all food products', img: cat },
            ],
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="accessory-arrival">
        <div v-for="info in info" class="father">
            <div>
                <img :src='info.img' />
                <div class="info">
                    <p>
                        {{ info.text }}
                    </p>
                    <h3>
                        {{ info.desc }}
                    </h3>
                    <Btn :text="info.btnText" bg="white" color="black" />
                </div>
            </div>
        </div>
    </div>


</template>

<style lang="scss">
.accessory-arrival {
    height: 100px;
    display: flex;
    margin-top: 230px;

    >.father {
        display: flex;
        width: 50%;
        align-items: center;
        justify-content: center;
        text-align: center;
        position: relative;

        .info {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
        }

        img {
            width: 100%;
        }
    }
}
</style>