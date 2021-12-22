<template>
    <div class="single-disc d-flex flex-column flex-grow-1 text-center">
        <div class="single-disc-image">
            <img :src="details.poster" alt="details.title">
        </div>
        <div class="single-disc-title">
            <h5>{{ details.title }}</h5>
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
    &-image{
        img{
            width: 100%;
            height: 100%;
            padding: 20px;
        }
        
    }
    &-title{
        color: white;
        text-transform: uppercase;
    }
    &-author{
        color: gray;
    }
    &-year{
        font-size: 13px;
        color: gray;
        padding-bottom: 20px;
    }
}
</style>