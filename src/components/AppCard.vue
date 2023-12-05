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
        <div v-if="item.price" class="card-content">
            <img :src="getImagePath(item.path)" alt="">
            <h3>{{ item.name }}</h3>
            <p class="price">{{ item.price }}</p>
        </div>
       
        <div class="alt-text" v-else>
            <div class="card-img">
                <img :src="getImagePath(item.path)" alt="">
            </div>
            
            <h3>{{ item.name }}</h3>
            <p>{{ item.text }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
h3, .price, .alt-text {
    text-align: center;
}
h3 {
    font-size: 1.6rem;
}
.price {
    color:#cc1a26;
}

.alt-text {
    h3 {
        font-size: 2.2rem;
        margin-bottom: 20px;
    }
    p {
        color: rgb(134, 134, 134);
    }
    .card-img {
        background-color: black;
        img {
        display: block;
        }
    }
    
    &:hover {
        img {
            opacity: 70%;
            
        }
    }
}

</style>