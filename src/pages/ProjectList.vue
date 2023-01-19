<template>
    <div>
        Sono Lista dei Progetti
    </div>
    <section>
        <div class="col-12 col-md-4" v-for="(project, index) in projects" :key="project.id">
                <ProjectCard :project="project"/>
        </div>
        <!-- <div>
        <div class="card" style="width: 18rem;" v-for="(project,index) in projects"  :key="index">
                    <div class="card-body">
                        <h5 class="card-title">{{project.title}}</h5>
                        <p class="card-text">{{ project.description}}</p>
                    </div>
        </div>
    </div> -->
    </section>
</template>

<script>
import ProjectCard from '../components/ProjectCard.vue';
import axios from 'axios';
import { store } from '../store';
    export default {
        name: 'ProjectList',
        components: {
            ProjectCard
        },
        data() {
            return {
                store,
                projects: []
            }
        },
        methods: {
            getProjects(){
                axios.get(`${this.store.apiBaseUrl}/projects`).then((response)=>{
                    this.projects = response.data.results;
                    console.log(response.data)
                })
            }
        },
        mounted(){
            this.getProjects();
        },
    }
</script>

<style lang="scss" scoped>

</style>