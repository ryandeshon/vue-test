<template>
    <ul class="list-group">
        <VideoListItem
            v-for="video in videos"
            :video="video"
            :key="video"
        />
    </ul>
</template>

<script>
import VideoListItem from './VideoListItem';
export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    props: {
        videos: Array
    },
    methods: {
    },
}
</script>

<style>
</style>