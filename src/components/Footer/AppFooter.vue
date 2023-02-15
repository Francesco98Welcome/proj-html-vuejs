<script>
import Btn from '../Shared/Btn.vue';

export default {
    name: 'AppFooter',
    data() {
        return {
            icons: [
                { imgIcon: 'fa-brands fa-facebook-f' },
                { imgIcon: 'fa-brands fa-twitter' },
                { imgIcon: 'fa-brands fa-instagram' },
                { imgIcon: 'fa-brands fa-youtube' }
            ],
        }
    },
    props: {
        menuItems: {
            type: Array,
        },
        menuItemsTwo: {
            type: Array
        },
        menuItemsThree: {
            type: Array
        }
    },
    components: {
        Btn
    }

}
</script>

<template>
    <footer>
        <div class="container-footer">

            <!-- PRIMA SEZIONE DEL FOOTER CON LOGO-->
            <div>
                <div class="img">
                    <img src="../../assets/categories/logo-footer.png">
                    <div>
                        1234 Avada Avenue Avadaville info@your-company.com<br> Call us: (1) 234 5678<br>
                    </div>
                </div>
            </div>

            <!-- SECONDA SEZIONE DEL FOOTER CON LINKS -->
            <div>
                <h2>
                    Shop by Brand
                </h2>
                <ul>
                    <a href="#">
                        <li v-for="item in menuItems">{{ item.item }}</li>
                    </a>
                </ul>
            </div>

            <!-- TERZA SEZIONE DEL FOOTER CON LINKS -->
            <div>
                <h2>
                    Useful Links
                </h2>
                <ul>
                    <a href="#">
                        <li v-for="item in menuItemsTwo">{{ item.linkUseful }}</li>
                    </a>
                </ul>
            </div>

            <!-- QUARTA SEZIONE DEL FOOTER CON REGISTRAZIONE - INPUT E BOTTONE -->
            <div>
                <div class="subscribe">
                    <span>Subscribe to our newsletter</span>
                    <input type="text" placeholder="Insert your email ...*">
                    <Btn text="Subscribe" bg="#3d6f42" color="white" />
                </div>
            </div>
        </div>

        <hr>

        <!-- LINK FINALI + ICONE -->

        <div class="links-footer">
            <ul>
                <li v-for="item in menuItemsThree">
                    {{ item.lastLinks }}
                </li>
            </ul>
            <div class="icons">
                <div v-for="icon in icons">
                    <i :class="icon.imgIcon"></i>
                </div>
            </div>
        </div>
    </footer>

    <div class="titoli-di-coda">
        <p>
            <i class="fa-solid fa-copyright"></i> Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights
            Reserved | Powered by WordPress
        </p>
    </div>
</template>

<style lang="scss" scoped>
footer {
    margin-top: 50px;
    height: 520px;
    background-color: $color_dark-green;
    color: white;
    font-size: 13px;


    .container-footer {
        height: 300px;
        width: 80%;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: center;
        justify-content: space-between;

        div {
            height: 200px;
            width: 250px;
            line-height: 2.5;
        }
    }

    .img img {
        width: 190px;
        margin-bottom: 20px;
        margin-top: 23px;
    }

    ul {
        list-style: none;

        a {
            text-decoration: none;
            color: white;
        }

    }

    h2 {
        margin-left: 38px;
    }

    .subscribe {
        margin-top: 15px;
        text-align: center;
        padding-top: 30px;
        border-radius: 10px;
        background-color: #264229;
        font-size: 18px;

        input {
            padding: 10px;
            border-radius: 20px;
            border: none;
            margin-top: 22px;
            margin-bottom: 14px;
        }

        button {
            width: 170px;
        }
    }

    hr {
        margin-top: 50px;
        width: 80%;
        background-color: #264229;
    }


    .links-footer {
        width: 30%;
        margin: 0 auto;
        margin-top: 30px;

        ul {
            display: flex;
            justify-content: space-around;
            list-style: none;
            padding: 0;

            >li:not(:first-child) {
                color: #b7b8b6
            }
        }
    }
}

.icons {
    display: flex;
    width: 25%;
    justify-content: space-between;
    margin: 0 auto;
    margin-top: 40px;

    i {
        font-size: 15px;
    }
}

.titoli-di-coda {
    padding: 10px;
    background-color: black;
    color: white;
    font-size: 10px;
    text-align: center;
}
</style>