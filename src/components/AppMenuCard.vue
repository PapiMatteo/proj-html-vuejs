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
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.card{
    position: relative;
    background-color: $baseImgBg;
    img {
        display: block;
        opacity: 60%;
        width: 100%;
        height: 200px;
    }
    h3{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: $primaryText;
    }
}
</style>