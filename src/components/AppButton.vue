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
@use "../style/partials/variables" as *;

p {
    color: $primaryText;
    background-color: $primaryBtn;
    padding: 10px 10px;
    border-radius: 20px;
    text-align: center;
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: 2px;
    a{
        display: inline-block;
        margin-right: 15px;
        text-decoration: none;
        color: $primaryText;
    }
    &:hover {
        & {
            background-color: $btnHover;
        }
    }
}

</style>