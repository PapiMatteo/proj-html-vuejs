<script>
import AppFooterBtn from './AppFooterBtn.vue';
import AppSocials from './AppSocials.vue';

export default {
    components: { AppFooterBtn, AppSocials }
}
</script>

<template>
    <div class="container">
        <img src="../assets/img/takeout-logo-2x-200x43.png" alt="">
        <div class="newsletter-text">
            <h1>Stay In The Loop</h1>
            <p>Sign up to receive up to date news and offers directly in your inbox</p>
        </div>
        <div class="sign-up">
            <input type="email" name="" id="" placeholder="you@email.com">
            <AppFooterBtn :btnText="'SUBSCRIBE'"/>
        </div>
        <AppSocials />
        
    </div>
</template>
    
<style lang="scss" scoped>

.container {
    width: 40%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    img {
        width: 200px;
        height: 43px;
        margin-bottom: 20px;
    }
    .newsletter-text {
        text-align: center;
        h1 {
            color: #fdc731;
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        p {
            color: white;
        }
    }
    
    .sign-up {
        width: 100%;
    }
    input {
        width: 100%;
        height: 50px;
        border-radius: 50px;
        padding: 15px;
        margin-bottom: 20px;
    }
}

</style>