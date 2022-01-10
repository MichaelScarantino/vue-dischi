<template>
    <div class="select-genre">
        <select @change="$emit('changeGenre', selectedGenre)" v-model="selectedGenre" name="" id="">
            <option value="all">All</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "Select",
    data: function () {
        return {
            selectedGenre: "",
        };
    },
}
</script>

<style scoped lang="scss">
@import "../style/variables";

.select-genre{
    margin-top: 10px;
}
</style>