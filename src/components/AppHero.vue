<script>
import AppButton from './AppButton.vue';
export default {
    components: {
        AppButton
    }
}
</script>

<template>
    <div class="container">
        <div class="hero-content">
            <div class="text-content">
                <p class="title-p">Hungry?</p>
                <h1>Great Food</h1>
                <h2>Delivered</h2>
                <AppButton :btnText="'VIEW OUR MENU'"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.hero-content {
    height: 600px;
    display: flex;
    align-items: center;
}
.text-content {
    color: white;
    letter-spacing: -3px;
    h1 {
        color: #fdc731;
        font-size: 4rem;
        
    }
    h2 {
        font-size: 3.5rem;
        margin-bottom: 1.2rem;
    }
    .title-p {
        font-size: 2rem;
    }

    p {
        width: 75%;
    }
}

</style>