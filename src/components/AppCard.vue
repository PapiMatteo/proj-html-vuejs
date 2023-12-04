<script>
export default {
    props:{
        item: Object
    },
    data() {
        return {
           
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
    <div class="card">
        <img :src="getImagePath(item.path)" alt="">
        <h3>{{ item.name }}</h3>
        <p class="price">{{ item.price }}</p>
    </div>
</template>

<style lang="scss" scoped>
h3, .price {
    text-align: center;
}
h3 {
    font-size: 1.6rem;
}
.price {
    color:#cc1a26;
}
img {
    width: 100%;
}
</style>