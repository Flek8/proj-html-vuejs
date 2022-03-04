<template>
    <div class="box">

        <div class="icons">
            
        </div>

        <div class="title">
            <i :class="'fa-solid ' + icon"></i><h3>{{title}}</h3>
        </div>

        <div class="text">
            <p>{{text}}</p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'MyBox',
    props: {
        icon: String,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    i {
        color: #048383;
    }

    h3 {
        display: inline-block;
        margin-left: 3px;
    }

    p {
        margin-top: 15px;
    }
</style>