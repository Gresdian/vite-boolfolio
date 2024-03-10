<script>
import { store } from '../store';
export default {
    name: 'SingleProject',
    props: {
        project: Object
    },
    data(){
        return {
            store
        }
    },
    methods: {
        createExcerpt() {
            return this.project.description.substr(0, 20) + '...';
        },
/*         getUrlImage(){
            if(this.project.cover_image != null) {
                image= '/storage/' + this.post.cover_image;
            }
            else {
                image = 'img/aaaa.jpg';
            }
            return `${this.store.baseurl}/storage/${image}`
        } */
    }

}
</script>
<template lang="">
    <div class="col-12 col-md-3">
        <div class="card m-3">
            <img :src="`${store.baseurl}/storage/${project.cover_image}`"  alt="" class="card-img-top">
            <div class="card-body">
                <h4>
                    {{ project.name }}
                </h4>
                <p>{{ createExcerpt() }}</p>
            </div>
        </div>

    </div>
</template>
<style lang="">
    
</style>