<template>
    <div class="image-container">
        <img
            :src="image.link"
            v-for="image in allImages"
            :key="image.name"
        />
    </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'
export default {
    name: 'ImageList',
    methods: mapActions(['fetchImages']),
    computed: mapGetters(['allImages']),
    created() {
        this.fetchImages();
    },
}
</script>

<style scoped>
.image-container {
    column-count: 3;
    column-gap: 0;
}
img {
    max-width: 100%;
    padding: 5px;
}
</style>