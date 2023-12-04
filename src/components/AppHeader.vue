<script>
export default {
    props: {
        navItems: Array
    }
}
</script>

<template>
    <header>
        <div class="container">

            <div class="header-content">
                <!-- Logo -->
                <a href=""><img src="../assets/img/takeout-logo-2x-200x43.png" alt=""></a>
                <ul>
                    <li v-for="item in navItems"><a href="">{{ item }}</a></li>
                    <li><a href=""><i class="fa-solid fa-cart-shopping"></i></a></li>
                </ul>
            </div>
            
        </div>
    </header>
    
</template>

<style lang="scss" scoped>
.container {
    width: 70%;
    margin: 0 auto;

    .header-content {
        height: 100px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    a {
        text-decoration: none;
        color: white;
    }
    ul {
        list-style-type: none;
        display: flex;
        gap: 2rem;
    }
}

</style>