<script>
import axios from 'axios';
import { store } from "../store";
import ProjectCard from "../components/ProjectCard.vue";

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
    },
    components: { ProjectCard }
}
</script>
<template>
    <div class="container my-3">
        <div class="row row-cols-lg-5 row-cols-md-4 row-cols-sm-3 g-3">
            <div v-for="project in projects" :key="project.id" class="col">
                <ProjectCard :project="project" />
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
h2 {
    color: purple;
}
</style>