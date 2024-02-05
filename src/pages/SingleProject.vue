<script>
import { store } from '../store';
import axios from 'axios';

export default {
    data() {
        return {
            store,
            project: {},
        }
    },
    created() {
        axios
            .get(`${this.store.baseUrl}/projects/${this.$route.params.slug}`)
            .then((resp) => {
                this.project = resp.data.results
                console.log(this.project);
            })
    }
}
</script>

<template>
    <div class="container my-3">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
    </div>
</template>

<style lang="scss" scoped>
    
</style>