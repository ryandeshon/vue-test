<template>
    <div v-if="video">
        <div class="details">
        <h4>{{ video.snippet.title }}</h4>
        <p>{{ video.snippet.descritption }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'VideoDetail',
    computed: {
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