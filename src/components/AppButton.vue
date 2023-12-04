<script>
export default {
    props: {
        btnText: String
    }
}
</script>

<template>
    <p><a href="">{{ btnText }}</a><i class="fa-solid fa-circle-arrow-right"></i></p>
</template>

<style lang="scss" scoped>
p {
    background-color: #cc1a26;
    padding: 10px 0;
    border-radius: 20px;
    text-align: center;
    font-size: 1.2rem;
    letter-spacing: normal;
    a{
        display: inline-block;
        margin-right: 15px;
        text-decoration: none;
        color: white;
    }
    &:hover {
        & {
            background-color: #bf1e23;
        }
    }
}

</style>