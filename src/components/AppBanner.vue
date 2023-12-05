<script>
export default {

}
</script>

<template>
    <div class="mobile-app">
        <div class="container">
            <div class="banner">
                <h2>Download Our</h2>
                <h1>Ordering App</h1>
                <div class="app-downloader">
                    <a href=""><img src="../assets/img/app-store-badge-200x67.png" alt=""></a>
                    <a href=""><img src="../assets/img/play-store-badge-200x67.png" alt=""></a>
                </div>
            </div>  
        </div>
    </div>
</template>

<style lang="scss" scoped>
.mobile-app {
    background-image: url('../assets/img/app-ordering-scaled.jpg');
    background-size: cover;
    height: 500px;
    .container{
        .banner {
            display: flex;
            flex-direction: column;
            height: 500px;
            justify-content: center;
            h2 {
                color: white;
                font-size: 2.5rem;
            }
            h1 {
                color: #fdc731;
                font-size: 4rem;
                margin-bottom: 2.5rem;
            }
            a{
                margin-right: 1rem;
            }
        }
    }
}
</style>