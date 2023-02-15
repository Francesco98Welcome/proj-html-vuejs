<script>
// immagini per la sezione delle categorie. prima sezione a partire dal main.
import cuscini from "../../../assets/categories/categories/cuscini200x200.jpg";
import osso from "../../../assets/categories/categories/osso200x200.jpg";
import palline from "../../../assets/categories/categories/palline200x200.jpg";
import borsa from "../../../assets/categories/categories/borsa200x200.jpg";

export default {
    name: 'Category',
    data() {
        return {
            // salvo i dati per la sezione delle categorie, prima sezione del main
            info: [
                { text: 'Bed(1)', img: cuscini },
                { text: 'Food(6)', img: osso },
                { text: 'Toys(6)', img: palline },
                { text: 'Trasport(6)', img: borsa },
            ],
        }
    },
}
</script>

<template>
    <div class="category">
        <div v-for="info in info">
            <div>
                <img :src='info.img' />
            </div>
            <div>
                {{ info.text }}
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.category {
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
</style>