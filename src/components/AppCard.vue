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
            <div class="card-img">
                <img :src="getImagePath(item.path)" alt="">
            </div>
            
            <div class="over-content">
                <p class="over-icon"><a href=""><i class="fa-regular fa-square-check"></i></a></p>
                <p><a href="">VIEW CART</a></p>
            </div>
            
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

.card-content {
    position: relative;

    .over-content {
        display: none;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        .over-icon {
            font-size: 3.2rem;
            background-color: rgba(0, 0, 0, 0.678);
            padding: 15px 20px;
            text-align: center;
            border-radius: 50%;
            color: white;
            margin-bottom: 20px;
        }
        a{
            text-decoration: none;
            color: white;
        }
    }

    &:hover {
        img {
            opacity: 60%;
        }
        .over-content {
            display: block;
        }
    }
    
}

.card-img {
    background-color: black;
    img {
        display: block;
    }
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
        width: 100%;
        }
    }
    
    &:hover {
        img {
            opacity: 70%;
            
        }
    }
}

</style>