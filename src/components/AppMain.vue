<script>
import AppPopular from './AppPopular.vue';

export default {
    components: { AppPopular }
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
</template>

<style lang="scss" scoped>

ul {
    list-style-type: none;
    height: 50px;
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