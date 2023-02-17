<script>
import cuscini from "../../../assets/categories/newproducts/cuscini300x300.jpg";
import palline from "../../../assets/categories/categories/palline300x300.jpg";
import osso from "../../../assets/categories/categories/osso300x300.jpg";
import borsa from "../../../assets/categories/newproducts/borsa300x300.jpg";
import gabbia from "../../../assets/categories/newproducts/gabbia300x300.jpg"
import gabbiagatto from "../../../assets/categories/newproducts/gattogabbia300x300.jpg"

import Btn from '../../Shared/Btn.vue';
export default {
    name: 'NewProductArrival',
    data() {
        return {
            info: [
                { text: 'Colored pet bed', price: '$18.00 - $26.00', img: cuscini },
                { text: 'Colorfull bet set', price: '$29.00', img: palline },
                { text: 'Dog bone', oldprice: '$29.00', price: '$18.00', img: osso, sale: true },
                { text: 'Animal trasport bag', price: '$25.00', img: borsa },
                { text: 'Animal trasport cage', price: '$35.00', img: gabbia },
                { text: 'Closable cat litter', price: '$16.00', img: gabbiagatto }

            ]
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="newproduct">
        <h1>New product arrivals</h1>
        <p>Lates products</p>

        <div class="new-products-arrivals">
            <div v-for="info in info" class="relative">
                <div class="image">
                    <img :src='info.img' />
                </div>
                <div class="text-price">
                    <div class="text">
                        {{ info.text }}
                    </div>
                    <div class="price">
                        <span class="old-price">{{ info.oldprice }}</span>
                        {{ info.price }}
                    </div>
                    <div v-if="info.sale" class="sale">
                        Sale!
                    </div>
                </div>
            </div>
        </div>
</div>
</template>

<style lang="scss">
.newproduct {
    padding-top: 20px;
    text-align: center;

    >h1 {
        font-family: 'Mali', cursive;
    }


    .new-products-arrivals {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;

        >div {
            width: calc(100% / 3);
            text-align: center;
        }

        .image {
            margin: 5px;

            img {
                width: 100%;
            }
        }

        .text-price {
            margin-top: 12px;
            margin-bottom: 15px;

            div {
                padding: 6px;
            }
        }
    }

    .relative {
        position: relative;
    }

    .sale {
        position: absolute;
        top: 2%;
        left: 3%;
        background-color: $color_light-green;
        color: white;
        border-radius: 20px;
    }
}
</style>