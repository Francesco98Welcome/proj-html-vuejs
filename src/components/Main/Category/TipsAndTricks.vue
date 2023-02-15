<script>
// immagini per la sezione delle categorie. prima sezione a partire dal main.
import catjump from "../../../assets/categories/tipsandtricks/catjump.jpg";
import catsleep from "../../../assets/categories/tipsandtricks/catsleep.jpg";
import girldog from "../../../assets/categories/tipsandtricks/girldog.jpg";
import kiddog from "../../../assets/categories/tipsandtricks/kiddog.jpg";

import Btn from "../../Shared/Btn.vue"

export default {
    name: 'TipsAndTricks',
    data() {
        return {
            // salvo i dati per la sezione delle categorie, prima sezione del main
            info: [
                { text: 'How to lose leash walk your dog', desc: 'April 21st, 2020', img: girldog },
                { text: 'Stop cats from scratching furniture', desc: 'April 19st, 2020', img: catjump },
                { text: 'Where to buy the best pet food', desc: 'April 18th, 2020', img: catsleep },
                { text: 'Proper care for your pet toys', desc: 'April 17th, 2020', img: kiddog },
            ],
        }
    },
    components: {
        Btn
    }
}
</script>

<template>
    <div class="section-tips-and-tricks">
        <h1>Get the best tips & tricks</h1>
        <h4>Recent articles</h4>
        <div class="tipsandtricks">
            <div v-for="info in info">
                <div>
                    <img :src='info.img' />
                </div>
                <div class="txt">
                    {{ info.text }}<br>
                    <span class="desc">{{ info.desc }}</span>
                </div>
            </div>
        </div>
        <Btn text="Read all articles" bg="#3d6f42" color="white" />
    </div>
</template>

<style lang="scss">
.section-tips-and-tricks {
    width: 80%;
    margin: 0 auto;
    margin-top: 70px;
    text-align: center;

    .tipsandtricks {
        display: flex;
        justify-content: space-between;

        >div {
            width: calc(100% / 4);
            margin: 0 auto;
            margin: 10px;

            img {
                width: 100%;
                margin-bottom: 15px;
            }

            .txt {
                padding-left: 15px;
                line-height: 1.5;
                width: 170px;
                text-align: left;

                .desc {
                    font-size: 10px;
                }
            }
        }
    }

    h1,
    h4 {
        text-align: center;
    }

    button {
        margin-top: 20px;
    }
}
</style>