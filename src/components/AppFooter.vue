<script>
import AppNewsletter from './AppNewsletter.vue';

export default {
    props: {
        navItem: Array
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    },
    components: { AppNewsletter }
}
</script>

<template>
    <footer>
        <div class="footer-container">
            <div v-for="item in navItem" class="list">
                <h4 :class="item.title == 'VOUCHER' ? 'voucher' : ''">{{ item.title }}</h4>
                <ul v-if="item.title !== 'OPENING HOURS'">
                    <li v-for="elem in item.navigation"><a href="">{{ elem }}</a></li>
                    <li v-if="item.imgList" v-for="img in item.imgList"><a href=""><img :src="getImagePath(img.imgPath)" alt="" :class="item.title == 'VOUCHER' ? 'coupon' : 'download'"></a></li>
                    <li v-if="item.title == 'VOUCHER'">
                        <p class="coupon-text">Just Use The Code</p>
                        <h2 class="coupon-title">FIRSTORDER</h2>
                        <p class="coupon-text bottom-text">At Checkout</p>
                    </li>
                </ul>
                <ul v-else>
                    <li v-for="elem in item.navigation">{{ elem.day }} <span class="hour">{{ elem.hour }}</span></li>
                </ul>
            </div>
        </div>

        <AppNewsletter />
        
        <p class="copyright"><span>&copy; Copyright 2012 - 2020 | Avada Theme by </span> ThemeFusion <span>| All Rights Reserved | Powered by</span> WordPress</p>

    </footer>

</template>

<style lang="scss" scoped>

footer {
    background-image: url('../assets/img/footer-background-scaled.jpg');
    background-size: cover;
    background-position: center;
    min-height: 1000px;
    

    .footer-container {
        width: 85%;
        margin: 0 auto;
        padding-top: 6rem;
        display: flex;
        justify-content: space-between;
        margin-bottom: 4rem;
    }

    .list{
        color: white;
        h4 {
            margin-bottom: 1.5rem;
            font-weight: 800;
        }
        .voucher {
            padding-left: 35px;
        }
        
        ul {
            list-style-type: none;
            li {
                margin-bottom: 1.5rem;
                font-weight: 600;
                &:hover {
                    a {
                        color: #fdc731;
                    }
                }
                .download {
                    width: 80%;
                    border: 2px solid white;
                    border-radius: 10px;
                }
                .coupon {
                    width: 80%;
                }
                .coupon-text {
                    font-weight: 600;
                    padding-left: 15px;
                }
                .coupon-title {
                    color: #fdc731;
                    padding-left: 10px;
                }
                
                .bottom-text {
                    padding-left: 38px;
                }
                .hour{
                    color: #fdc731;
                }
            }
        }
        a{
            text-decoration: none;
            color: inherit;
        }
    }
    .copyright {
        color: white;
        text-align: center;
        padding-top: 20px;
        font-size: .6rem;
    }
    span {
        color: #fdc731;
    }
}

</style>