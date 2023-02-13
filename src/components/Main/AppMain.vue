<script>
// importo i vari componenti di cui ho bisogno.
import Categories from './Category/Categories.vue';
import FoodSection from './Category/FoodSection.vue';

// immagini per la sezione delle categorie. prima sezione a partire dal main.
import cuscini from "../../assets/categories/categories/cuscini200x200.jpg";
import osso from "../../assets/categories/categories/osso200x200.jpg";
import palline from "../../assets/categories/categories/palline200x200.jpg";
// import borsa from "../../assets/borsa500x500.jpg";

// immagini per la sezione del cibo, la seconda sezione del main.
import kibble from "../../assets/categories/food/kibble420x400.png";
import moist from "../../assets/categories/food/moist210x200.png";
import frozen from "../../assets/categories/food/frozen200x210.png";

export default {
    name: 'AppMain',
    data() {
        return {
            // salvo i dati per la sezione delle categorie, prima sezione del main
            CategoryInfo: [
                { text: 'Bed(1)', img: cuscini },
                { text: 'Food(6)', img: osso },
                { text: 'Toys(6)', img: palline },
                { text: 'Trasport(6)'/* , img: borsa */ },
            ],
            // salvo i dati per la sezione dei cibi, seconda sezione di immagini del main
            FoodSection: [
                { text: 'Kibble', desc: 'Dry dog food'/*, img: kibble*/ },
                { text: 'Moist', desc: 'Canned dog food', img: moist },
                { text: 'Frozen', desc: 'Freeze-Dried dog food', img: frozen }
            ]
        }
    },
    components: {
        Categories,
        FoodSection
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


        <div class="second-section-food">
            <FoodSection :info="FoodSection" />
        </div>

    </main>

</template>

<style lang="scss" scoped>
.init-main {
    margin-top: 30px;
    width: 400px;
    margin: 0 auto;
    text-align: center;
    border: 1px solid black;
    margin-top: 40px;

    * {
        padding-top: 10px;
    }
}


// regole stile per la prima sezione di foto della parte del Main
.first-section,
.second-section-food {
    width: 71%;
    margin: 0 auto;
    margin-top: 40px;
    border: 1px solid black;
}
</style>