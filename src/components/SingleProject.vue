<script>
export default {
    name: 'SingleProject',
    props: {
        project: Object
    },

}
</script>
<template lang="">
    <div class="card">
        <img :src="project.cover_image" alt="" class="card-img-top">
        <div class="card-body">
            <h4>
                {{ project.name }}
            </h4>
        </div>
    </div>
</template>
<style lang="">
    
</style>