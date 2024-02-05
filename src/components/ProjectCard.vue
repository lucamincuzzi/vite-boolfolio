<script>
import axios from 'axios';

export default {
    props: {
        project: Object,
    },
    data() {
        return {

        }
    },
}
</script>

<template>
    <div class="card h-100">
        <div class="card-body">
            <h4>{{ project.title }}</h4>
            <p>{{ project.description }}</p>
            <router-link :to="{ name: 'single-project', params: {slug: project.slug} }">Dettagli</router-link>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.col {
    max-height: 300px;
}
</style>