<script>
export default {
    name: 'Items',
    data() {
        return {
        }
    },
    props: {
        info: {
            type: Array,
        }
    },
}
</script>

<template>

    <div class="usersTestimonials">
        <h2>Users Testimonials</h2>
        <div class="users">
            <div class="face-text-user">
                <div class="face-user">
                    <img src="../../../assets/categories/users-testimonials/girlcat200x200.jpg">
                </div>
                <div>
                    Auctor est habitasse amet nunc, interdum vel mattis sodales crea. Ut nulla quis nunc, ticindunt
                    eu.
                    Eu.
                </div>
                <div>
                    Lisa Smith, Themefusion
                </div>
            </div>
            <div class="face-text-user">
                <div class="face-user">
                    <img src="../../../assets/categories/users-testimonials/donnasmile200x200.jpg">
                </div>
                <div>
                    Donec sollicitudin molestie malesuada. Vivamus suscipit tortor eget felis porttitor volutpat
                    vestibulum ac diam sit.
                </div>
                <div>
                    Lisa Smith, Themefusion
                </div>
            </div>
            <div class="face-text-user">
                <div class="face-user">
                    <img src="../../../assets/categories/users-testimonials/boydog200x200.jpg">
                </div>
                <div>
                    Curabitor arcu erat, accumsan id imperdied et, porttitor at sem. Proin eget tortor risus vestibulum
                    ante ipsum
                </div>
                <div>
                    Sam Lewis, ThemeFusion
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.usersTestimonials {
    padding-top: 30px;
    padding-bottom: 130px;
    margin: 50px auto 0;
    background-color: $color_dark-green;
    color: white;

    h2 {
        text-align: center;
        margin-top: 50px;
    }

    .users {
        width: 80%;
        margin: 0 auto;
        margin-top: 30px;
        display: flex;
        justify-content: space-between;

        .face-text-user {
            text-align: center;

            >div {
                margin-bottom: 20px;
            }

            >div:last-child {
                color: rgb(152, 148, 148);
            }
        }

        >div {
            width: 32%;
            line-height: 1.5;
            font-size: 15px;
            padding: 13px;

            .face-user {
                border-radius: 50px;
                height: 80px;
                width: 80px;
                margin: 0 auto;
                margin-bottom: 20px;
                margin-top: 20px;

                img {
                    width: 100%;
                    border-radius: 50px;
                }
            }
        }
    }
}
</style>