<template>
    <section>
        <div class="wrapper">
            <div class="container-fluid">
                <Select @changeGenre="changePerformed" />
            </div>
        </div>
        <div class="wrapper">
            <div class="container-fluid">
                <div v-if="!isLoading" class="row row-cols-5">
                    <div v-for="(disc, index) in filteredGenre" :key="index" class="col d-flex flex-column align-items-stretch">
                        <SingleDisc :details="disc" />  
                    </div>
                </div>
                <Loader v-else />
            </div>
        </div>
        
    </section>
</template>

<script>
import axios from 'axios';
import SingleDisc from "../components/SingleDisc.vue"
import Select from "./Select.vue"
import Loader from "./Loader.vue"


export default {
    name: "DiscsList",
    components: {
        SingleDisc,
        Select,
        Loader
    },
    data: function() {
        return {
            discs: [],
            changedGenre: "",
            isLoading: true,
        }
    },
    methods: {
        changePerformed: function(text) {
            this.changedGenre = text;
        },
    },
    computed: {
        filteredGenre: function() {
            if( (this.changedGenre === '') || (this.changedGenre === 'all') ){
                return this.discs;
            }
            const filterGenreArray = this.discs.filter( (element) => {
                return element.genre.toLowerCase().includes(this.changedGenre.toLowerCase())
            });

            return filterGenreArray;
        }
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then( (response) => {
            this.discs = response.data.response;
            this.isLoading = false;
        });
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables";

</style>