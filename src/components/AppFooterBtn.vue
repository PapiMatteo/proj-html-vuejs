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
@use "../style/partials/variables" as *;

p {
    color: $primaryText;
    background-color: $primaryBtn;
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
        color: $primaryText;
    }
    &:hover {
        & {
            background-color: $btnHover;
        }
    }
}

</style>