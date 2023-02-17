<script>
// importo i vari componenti di cui ho bisogno.
import Btn from '../Shared/Btn.vue';
import Categories from './Category/Categories.vue';
import FoodSection from './Category/FoodSection.vue';
import Items from './Category/Items.vue';
import UsersTestimonials from './Category/UsersTestimonials.vue';
import NewsLetter from './Category/NewsLetter.vue';
import TipsAndTricks from './Category/TipsAndTricks.vue';
import AccessoryArrival from './Category/AccessoryArrival.vue';
import NewProductArrival from './Category/NewProductArrival.vue';

export default {
    name: 'AppMain',
    data() {
        return {
        }
    },
    components: {
        Categories,
        FoodSection,
        Btn,
        Items,
        UsersTestimonials,
        NewsLetter,
        TipsAndTricks,
        AccessoryArrival,
        NewProductArrival
    }

}
</script>

<template>
    <main>
        <div class="init-main">
            <h3>Browse by category</h3>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. In adipisci est soluta illum non nobis itaque
            </p>
        </div>

        <!-- prima sezione con foto del main, cuscini, osso, palline, borsa -->

        <div class="first-section">
            <Categories :info="CategoryInfo" />
        </div>

        <!-- seconda sezione con foto dei croccantini -->

        <div class="second-section-food">
            <FoodSection :info="FoodSection" />
        </div>

        <div class="new-arrivals">
            <div class="new-arrivals-text">
                New arrivals weekly
                <div>
                    <Btn text="Learn more about us" bg="white" color="black" />
                </div>
            </div>
        </div>

        <div class="items-section">
            <Items :info="ItemsSection" />
        </div>

        <UsersTestimonials />

        <NewsLetter />

        <TipsAndTricks />

        <AccessoryArrival />

        <NewProductArrival />
    </main>

</template>

<style lang="scss" scoped>
.init-main {
    margin-top: 30px;
    width: 400px;
    margin: 0 auto;
    text-align: center;
    margin-top: 40px;

    h3 {
        font-family: 'Mali', cursive;
        font-size: 30px;
    }

    * {
        padding-top: 10px;
    }
}

// regole stile per la prima sezione di foto della parte del Main

.first-section,
.second-section-food,
.new-arrivals,
.items-section {
    width: 80%;
    margin: 0 auto;
    margin-top: 40px;
}

.new-arrivals {
    height: 330px;
    position: relative;
    font-size: 35px;

    background-image: url('../../assets/categories/animals/dogsLove.jpg');
    background-size: cover;
    background-repeat: no-repeat;

    .new-arrivals-text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: white;
        font-family: 'Mali', cursive;

        >div:last-child {
            text-align: center;

            button {
                margin-top: 20px;
                padding: 6px;
                color: black;
            }
        }
    }
}
</style>