<template>
    <div class="box">

        <div class="icons">
            <i id="icon-big" :class="'fa-solid ' + iconTop"></i>
            <i :class="'fa-solid ' + iconArrow"></i>
        </div>

        <div class="title">
            <span><i v-if="icon" :class="'fa-solid ' + icon"></i></span> <h3>{{title}}</h3>
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
        iconArrow: String,
        iconTop: String,
        icon: String,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    #icon-big {
        font-size: 20px;
    }

    .icons {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        color: #048383;
    }

    h3 {
        display: inline-block;
    }

    .title span {
        color: #048383;
    }
</style>