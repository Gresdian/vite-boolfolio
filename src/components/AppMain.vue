<script>
import SingleProject from './SingleProject.vue';
import { store } from '../store.js';
import axios from 'axios';
export default {
    name: 'AppMain',
    components:{
        SingleProject
    },
    data() {
        return{
            store,
            projects: []
        }
    }, 
    created(){
        this.getProjects();
    },
    methods: {
        getProjects(){
            axios.get(`${this.store.baseurl}/api/projects`).then((response) => {
                this.projects = response.data.results;
            })
        }
    },
}
</script>
<template lang="">
    <div class="mt-5 ">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1 class="text-center ">Boolfolio</h1>
                </div>
            </div>
            <div class="row">
                <SingleProject v-for = "project, index in projects" :key="index" :project="project" />
            </div>
        </div>
    </div>
</template>
<style lang="">
    
</style>