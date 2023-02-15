<script>
import gabbia from "../../../assets/categories/items/gabbia200x200.jpg";
import dogleashpink from "../../../assets/categories/items/collarerosa200x200.jpg";
import gabbiaperta from "../../../assets/categories/items/gabbiaaperta200x200.jpg";
import collarecolorato from "../../../assets/categories/items/collarecolorato200x200.jpg"

import Btn from '../../Shared/Btn.vue';
export default {
    name: 'Items',
    data() {
        return {
            info: [
                { text: 'Trasport cage', price: '$25.00', img: gabbia },
                { text: 'Dog leash', price: '$25.00', img: dogleashpink },
                { text: 'Animal trasport cage', oldprice: '$35.00', price: '$25.00', img: gabbiaperta },
                { text: 'Colorful cat leash', price: '$12.00', img: collarecolorato }
            ]
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="intro-items-section">
        <h2>Items everyone loves</h2>
        <div>
            <Btn text="View all products" bg="#3d6f42" color="white" />
        </div>
    </div>
    <div class="items">
        <div v-for="info in info">
            <div>
                <img :src='info.img' />
            </div>
            <div>
                {{ info.text }}
            </div>
            <div>
                <span class="old-price">{{ info.oldprice }}</span>
                {{ info.price }}
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.intro-items-section {
    display: flex;
    border: 1px solid black;
    justify-content: space-between;
    align-items: center;
    margin: 50px 0;
}

.items {
    display: flex;
    justify-content: space-between;

    >div {
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

.old-price {
    text-decoration: line-through;
    font-size: 14px;
}
</style>