<script>
export default {
    props: {
        btnText: String
    }
}
</script>

<template>
    <p><a href="">{{ btnText }}</a></p>
</template>

<style lang="scss" scoped>
p {
    color: white;
    background-color: #cc1a26;
    padding: 15px 0;
    border-radius: 20px;
    text-align: center;
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: 2px;
    width: 100%;
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