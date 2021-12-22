<template>
    <header>
        <div class="header-logo">
            <img src="../assets/img/logo.png" alt="Logo Spotify">
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
}
</script>

<style scoped lang="scss">
@import "../style/variables";
header{
    width: 100%;
    height: 80px;
    background-color: $brand_primary_color;
    line-height: 80px;

    .header-logo{
        width: 50px;
        margin-left: 20px;
    }
}

</style>