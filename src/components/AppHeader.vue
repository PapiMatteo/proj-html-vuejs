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


.header-content {
    padding-top: 1.5rem;
    height: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    ul {
        list-style-type: none;
        display: flex;
        gap: 2rem;

        li {
            font-weight: 600;
            color: white;
            a {
                text-decoration: none;
                color: inherit;
            }

            &:hover {
                color: #fdc731;
            }
        }
    }

}
    

</style>