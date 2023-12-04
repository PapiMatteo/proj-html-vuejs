<script>
import AppButton from './AppButton.vue';
import AppCard from './AppCard.vue';

export default {
    components: {
    AppCard,
    AppButton
},
    data() {
        return {
            imgList: [
                {  
                    path: 'skin-on-fries.jpg',
                    name: 'Skin On Fries',
                    price: '$4.99'
                },
                {
                    path:'choco-cookie-frappe.jpg',
                    name: 'Choco Cookie Frappe',
                    price: '$3.00 - $6.00'
                },
                {
                    path: 'donut-burger.jpg',
                    name: 'Donut Burger',
                    price: '$6.99'
                }
            ]
        }
    }
}
</script>

<template>
    <h2>Our Most Popular Dishes</h2>
    <div class="row">
        <div v-for="item in imgList" class="col">
            <AppCard :item="item"/>
        </div>
    </div>
    <div class="btn">
        <AppButton :btnText="'START YOUR ORDER'"/>
    </div>

    
    
</template>

<style lang="scss" scoped>
h2 {
    text-align: center;
    font-size: 2rem;
    margin: 3rem 0;
}
.row {
    display: flex;
    gap: 1.5rem;   
    margin-bottom: 2rem;
}

.btn {
    display: flex;
    justify-content: center;   
}


</style>