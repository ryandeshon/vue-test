<template>
    <div v-if="video" class="col-md-8">
        <div class="details">
            <div class="embed-responsive embed-responsive-16by9">
                <iframe class="embed-responsive-item" :src="video.snippet.url" frameborder="0" />
            </div>
            <h4>{{ video.snippet.title }}</h4>
            <p>{{ video.snippet.descritption }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'VideoDetail',
    computed: {
        videoUrl() {
            const { videoId } = this.video.id;
            return `https://www.youtube.com/embed/${videoId}`;
        }
    },
    props: {
        video: Array
    },
    methods: {
    },
}
</script>

<style scoped>
    .details {
        margin-top: 1rem;
        padding: 1rem;
        border: 1px solid #ddd;
        border-radius: 1rem;
    }
</style>