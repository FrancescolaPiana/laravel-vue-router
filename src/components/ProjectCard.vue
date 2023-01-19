<template>
    <div>
        <div class="card" style="width: 18rem;">
                    <!-- <img :src="`${store.imagBasePath}${project.cover_image}`" class="card-img-top" :alt="project.title"> -->
                    <div class="card-body">
                        <h5 class="card-title">{{project.title}}</h5>
                        <p class="card-text">{{ project.description }}</p>
                        <!-- <router-link class="btn btn-primary" :to="{name: 'single-project', params:{slug: project.slug}}">
                        Vedi il project
                        </router-link>                     -->
                    </div>
                </div>
    </div>
</template>

<script>
import {store} from '../store';
export default {
        name: 'ProjectCard',
        props: ['project'],
        data() {
            return {
                store
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>