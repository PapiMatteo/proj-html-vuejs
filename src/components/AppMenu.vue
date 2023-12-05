<script>
import AppButton from './AppButton.vue';
import AppMenuCard from './AppMenuCard.vue';

export default {
    components: {
    AppButton,
    AppMenuCard
},
    data() {
        return {
            menuList: [
                {
                    path: 'appetizers-menu-background.jpg',
                    name: 'APPETIZER'
                },
                {
                    path: 'burgers-menu-background.jpg',
                    name: 'BURGERS'
                },
                {
                    path: 'pizza-menu-background.jpg',
                    name: 'PIZZAS'
                },
                {
                    path: 'fries-menu-background.jpg',
                    name: 'FRIES'
                },
                {
                    path: 'sides-menu-background.jpg',
                    name: 'SIDES'
                },
                {
                    path: 'desserts-menu-background.jpg',
                    name: 'DESSERTS'
                },
                {
                    path: 'beverages-menu-background.jpg',
                    name: 'BEVERAGES'
                },
                {
                    path: 'specials-menu-background.jpg',
                    name: 'SPECIALS'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="title-zone">
            <h2>Menu Categories</h2>
            <AppButton :btnText="'VIEW FULL MENU'"/>
        </div>
        <div class="row">
            <div v-for="item in menuList" class="col">
                <AppMenuCard :item="item"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.title-zone {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 9rem;
    margin-bottom: 3rem;
    h2 {
        font-size: 2rem;
    }
}

.row {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    margin-bottom: 4rem;
    .col {
        width: calc((100% / 4) - 2rem);   
    }
}
</style>