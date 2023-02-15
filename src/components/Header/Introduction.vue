<script>
import Btn from '../Shared/Btn.vue';

export default {
    name: 'Introduction',
    data() {
        return {
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="hero">
        <div class="partOne">
            <ul>
                <li><i class="fa-regular fa-map"></i> International Shipping Services</li>
                <li><i class="fa-sharp fa-regular fa-clock"></i> See our store houres and services</li>
                <li><i class="fas fa-check"></i> We price match to give you the best deals</li>
            </ul>
        </div>
        <div class="sfondo">

            <div class="text">
                <h2>We know animals are a part of your family, let us help take care of them</h2>
                <Btn text="Learn more about us" bg="white" />
            </div>

        </div>

        <div class="partTwo">
            <img src="../../assets/categories/food/littlefoodimage.png">
            <p>Get $25 OFF your first purchase of our homemade pet food!</p><a href="#">Visit the shop!</a>
        </div>
    </div>

</template>


<style lang="scss">
.hero {
    border: 1px solid black;
    height: 750px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .sfondo {
        background-image: url('../../assets/categories/sfondoIntroduction.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 100%;
        padding-top: 10%;
    }

    .partOne {
        padding: 6px;
        color: white;
        background-color: $color_dark-green;

        ul {
            display: flex;
            list-style: none;
            justify-content: space-around;
            font-size: 14px;
        }
    }

    .partTwo {
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        background-color: $color_dark-green;
        color: white;

        >img {
            width: 150px;
            margin-right: 30px;
            margin-top: 20px;
        }

        >a {
            margin-left: 30px;
            color: rgb(130, 127, 127);
        }
    }

    .text {
        margin-left: 140px;
        width: 400px;

        h2 {
            font-size: 40px;
            color: white;
        }
    }
}
</style>
