<template>
    <section>
        <div class="wrapper">
            <div class="container-fluid">
                <div class="row row-cols-5">
                    <div v-for="(disc, index) in discs" :key="index" class="col d-flex flex-column align-items-stretch">
                        <SingleDisc :details="disc" />  
                    </div>
                </div>
            </div>
        </div>
        
    </section>
</template>

<script>
import SingleDisc from "../components/SingleDisc.vue"
import axios from 'axios';
export default {
    name: "DiscsList",
    components: {
        SingleDisc,
    },
    data: function() {
        return {
            discs: [],
        }
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then( (response) => {
            this.discs = response.data.response;
        });
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables";

.wrapper{
    width: 60%;
    margin: 50px auto;
}

</style>