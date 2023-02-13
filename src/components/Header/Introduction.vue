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
                <li>International Shipping Services</li>
                <li>See our store houres and services</li>
                <li>We price match to give you the best deals</li>
            </ul>
        </div>

        <div class="text">
            <h2>We know animals are a part of your family, let us help take care of them</h2>
            <Btn />
        </div>

        <div class="partTwo">
            Get $25 OFF your first purchase of our homemade pet food!
        </div>
    </div>

</template>


<style lang="scss">
.hero {
    border: 1px solid black;
    height: 600px;
    display: flex;
    flex-direction: column;

    justify-content: space-between;

    .partOne {
        border: 1px solid black;
        padding: 14px;

        ul {
            display: flex;
            list-style: none;
            justify-content: space-around
        }
    }

    .partTwo {
        border: 1px solid black;
        padding: 20px;
        text-align: center;
    }

    .text {
        border: 1px solid black;
        margin-left: 200px;
        width: 380px;
        min-height: 100px;

        h2 {
            font-size: 30px;
        }
    }
}
</style>
