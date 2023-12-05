<script>
import AppMenu from './AppMenu.vue';
import AppPopular from './AppPopular.vue';
import AppBanner from './AppBanner.vue';
import AppNews from './AppNews.vue';

export default {
    components: {
    AppPopular,
    AppMenu,
    AppBanner,
    AppNews
},
    data() {
        return {
            allergensList: [
                {
                    path: 'plant.png',
                    text: 'Vegetarian'
                },
                {
                    path: 'wheat.png',
                    text: 'Gluten Free'
                },
                {
                    path: 'lactose-free.png',
                    text: 'Dairy Free'
                },
                {
                    path: 'steak.png',
                    text: 'Keto Friendly'
                }
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="container">
        <ul>
            <li><i class="fa-regular fa-clock"></i> 24/7 DELIVERY</li>
            <li><i class="fa-solid fa-burger"></i> OVER 100 DISHES</li>
            <li><i class="fa-solid fa-mobile-screen-button"></i> IN APP ORDERING</li>
            <li><i class="fa-solid fa-car"></i> FAST DELIVERY</li>
        </ul>
        <AppPopular/>       
    </div> 
    <div class="sale-bg">
        <img src="../assets/img/svg-0.svg" alt="">
    </div>
    <AppMenu />
    <div class="container">
        <ul class="allergen">
            <li v-for="item in allergensList">
                <img :src="getImagePath(item.path)" alt="">
                <h4>{{ item.text }}</h4>
            </li>
        </ul>
    </div>
    <AppBanner />
    <AppNews />
</template>

<style lang="scss" scoped>

ul {
    list-style-type: none;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: white;
    padding-top: 20px;
    position: relative;
    top: -20px;
    color: rgb(41, 41, 41);
    li {
        font-size: .8rem;
        font-weight: 600;
        i {
            font-size: 1.2rem;
            margin-right: 5px;
        }
    }
}

.allergen {
    li {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
        img {
            height: 70px;
            width: 70px;
        }
        h4 {
            font-size: 1.5rem;
        }
    }
    margin-bottom: 5rem;
}

.sale-bg {
    background-image: url('../assets/img/first-order-background-scaled.jpg');
    height: 400px;
    background-position: center;
    background-size: cover;
    margin-top: 2rem;
    img {
        width: 100%;
        height: 150px;
    }
}


</style>