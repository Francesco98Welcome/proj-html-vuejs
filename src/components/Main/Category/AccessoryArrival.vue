<script>

import dog from "../../../assets/categories/animals/dogball.jpg";
import cat from "../../../assets/categories/animals/catwhite.jpg";

import Btn from '../../Shared/Btn.vue';

export default {
    name: 'AccessoryArrival',
    data() {
        return {
            infos: [
                { text: 'find the best animal supplies', desc: 'popular accessories', btnText: 'View all toys accessories', img: dog },
                { text: 'find the best food', desc: 'new food arrival', btnText: 'View all food products', img: cat },
            ],
            icons: [
                { text: 'Free worldwide deliveries', imgIcon: 'fa-sharp fa-solid fa-truck' },
                { text: 'Find stores near you', imgIcon: 'fa-regular fa-map' },
                { text: 'Best price guarranted', imgIcon: 'fa-sharp fa-solid fa-dollar-sign' },
                { text: 'All credit card accepted', imgIcon: 'fa-solid fa-credit-card' }
            ],
        }
    },
    components: {
        Btn,
    }
}
</script>

<template>
    <!-- sezione cane e gatto -->

    <div class="accessory-arrival">
        <div v-for="info in infos" class="container">
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

    <!-- sezione icone -->

    <div class="container-icons">
        <div class="icons">
            <div v-for="icon in icons">
                <div>
                    <i :class="icon.imgIcon"></i>
                </div>
                <div>
                    <p> {{ icon.text }}</p>
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

    >.container {
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

.container-icons {
    height: 190px;
    border: 1px solid black;
    display: flex;
    align-items: center;
    color: black;
    margin-top: 157px;
    background-color: $color_dark-green;
    color: white;

    .icons {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;

        div {
            text-align: center;

            p {
                font-size: 13px;
            }
        }

        i {
            font-size: 30px;
        }
    }
}
</style>