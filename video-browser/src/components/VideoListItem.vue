<template>
    <li class="list-group-item media">
        <img :src="videoThumbUrl" class="mr-3"/>
        <div class="media-body">{{ video.snippet.title }}</div>
    </li>
</template>

<script>
export default {
    name: 'VideoListItem',
    computed: {
        videoThumbUrl() {
            return this.video.snippet.thumbnails.default.url
        }
    },
    props: {
        video: Array
    },
}
</script>

<style scoped>
    li {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
    }
    li:hover {
        background-color: #eee;
    }
</style>