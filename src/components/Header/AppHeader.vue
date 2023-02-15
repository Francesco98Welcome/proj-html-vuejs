<script>

import Introduction from './Introduction.vue';

export default {
    name: 'AppHeader',
    data() {
        return {
        }
    },
    props: {
        menuItems: {
            type: Array,
        }
    },
    components: {
        Introduction
    }
}
</script>

<template>
    <header>
        <div class="container-header">
            <div>
                <img src="../../assets/categories/logoheader.png">
            </div>
            <div class="btn-search-header">
                <div class="btn-search">
                    <div><i class="fa-solid fa-magnifying-glass"></i></div>
                    <div><input type="text" placeholder="Search.."></div>
                </div>
            </div>
            <div><strong>Questions?</strong> Call us : 1.800.123.4567</div>
            <div>icon <i class="fa-solid fa-user"></i></div>
        </div>
        <hr>


        <div class="links-header">
            <ul>
                <li v-for="item in menuItems">{{ item.text }}</li>
            </ul>
        </div>

        <Introduction />
    </header>

</template>

<style lang="scss" scoped>
.container-header {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-top: 18px;
    padding-bottom: 8px;
    width: 90%;
    margin: 0 auto;

    >div>img {
        width: 200px;
    }

    .btn-search {
        display: flex;
        width: 300px;
        padding: 10px;
        border-radius: 30px;
        background-color: #f3f4f3;

        >div>input {
            border: none;
            margin-left: 10px;
            background-color: #f3f4f3;
        }
    }
}

.links-header>ul {
    display: flex;
    justify-content: center;
    list-style: none;

    li {
        padding-right: 40px;
        cursor: pointer;
    }

    >:not(:first-child) {
        color: #c1c1c1;
    }
}
</style>