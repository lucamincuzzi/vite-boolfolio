<script>
import axios from 'axios';
import { store } from "../store.js";

export default {
    data() {
        return {
            store,
            projects: [],
        }
    },
    created() {
        axios
        .get(`${this.store.baseUrl}/projects`)
        .then((resp) => {
            this.projects = resp.data.results;
            console.log(this.projects);
        })
    }
}
</script>
<template>
    <h2>My first component</h2>
</template>
<style lang="scss" scoped>
h2 {
    color: purple;
}
</style>