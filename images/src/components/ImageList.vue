<template>
    <div>
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
</style>