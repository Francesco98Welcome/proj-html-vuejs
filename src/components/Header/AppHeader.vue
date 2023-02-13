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
            <div>avada</div>
            <div>search</div>
            <div>questions? call us: 3490703987</div>
            <div>icon icon</div>
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
    padding: 15px;
}

.links-header>ul {
    display: flex;
    justify-content: center;
    list-style: none;

    li {
        padding: 10px;
    }
}
</style>