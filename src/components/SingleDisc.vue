<template>
    <div class="single-disc d-flex flex-column flex-grow-1 text-center">
        <div class="single-disc-image">
            <img :src="details.poster" :alt="details.title">
        </div>
        <div class="single-disc-title">
            <h2>{{ details.title }}</h2>
        </div>
        <div class="single-disc-author">
            {{ details.author }}
        </div>
        <div class="single-disc-year">
            {{ details.year }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'SingleDisc',
    props: ['details'],
}
</script>

<style scoped lang="scss">
@import "../style/variables";

.single-disc{
    background-color: $brand_primary_color;
    margin: 10px 0;
    padding: 5px;

    &-image{
        img{
            width: 100%;
            height: 100%;
            padding: 10px;
        }
        
    }
    &-title{
        color: white;
        text-transform: uppercase;
        h2{
        font-size: 16px;

        }
    }
    &-author{
        color: gray;
        font-size: 12px;
    }
    &-year{
        font-size: 13px;
        color: gray;
        padding-bottom: 10px;
    }
}
</style>