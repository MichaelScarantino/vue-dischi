<template>
    <div class="loader">
        Loading...
    </div>
</template>

<script>
export default {
    name: "Loader",
}
</script>

<style scoped lang="scss">
@import "../style/variables";

.loader{
    font-size: 30px;
    color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(- 50%, - 50%);
}
</style>