<script>
import AppButton from './AppButton.vue';
import AppCard from './AppCard.vue';

export default {
    components: { 
        AppButton, 
        AppCard 
    },
    data() {
        return {
            newsInfo: [
                {
                    path: 'pancake-burger-600x450.jpg',
                    name: 'NEW: The Pancake Burger',
                    text: 'Lorem ipsum dolor sit amet, consectetur adispiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi.'
                },
                {
                    path: 'new-milkshake-menu-600x450.jpg',
                    name: 'New Milkshake Menu',
                    text: 'Lorem ipsum dolor sit amet, consectetur adispiscing elit. Morbi sodales ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. Pellentesque commodo tortor vel mi.'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="title-and-btn">
            <h2>Latest News</h2>
            <AppButton :btnText="'READ MORE NEWS'"/>
        </div>
        <div class="row">
            <div v-for="item in newsInfo" class="col">
                <AppCard :item="item"/>
            </div>
        </div>
    </div>
    

</template>

<style lang="scss" scoped>
.title-and-btn {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 3rem;
    h2 {
        font-size: 2.5rem;
    }
}

.row {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 8rem;
}


</style>