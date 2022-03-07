<template>
    <div class="thumb">
        <img :src="require('../../assets/img/news-'+ photo +'.jpg')">
        <div class="overlay"></div>
        <span>{{text}}</span>
    </div>
</template>

<script>
export default {
    name: 'MyThumbnail',
    props: {
        photo: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    .thumb {
        width: calc((100% - 30px)/3);
        position: relative;
        border-radius: 10px;

        &:hover .overlay {
            display: none;
        }

        img {
            width: 100%;
            height: 100%;
            border-radius: 10px;
        }

        .overlay {
            width: 100%;
            height: 100%;
            border-radius: 10px;
            background-color: rgba(0, 0, 0, 0.60);
            position: absolute;
            left: 0;
            top: 0;
            z-index: 9;
        }

        span {
            position: absolute;
            color: white;
            bottom: 10%;
            font-weight: bold;
            left: 50%;
            transform: translate(-50%, 0);
            z-index: 99;
        }
    }
</style>