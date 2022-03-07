<template>
    <div>
        {{msg}}
    </div>
</template>

<script>
export default {
    name: 'MyButton',
    props: {
        msg: String
    }
}
</script>

<style scoped lang="scss">
    div {
        padding: 10px 15px;
        background-color: #048383;
        border: 1px solid #048383;
        color: white;
        border-radius: 3px;
        display: inline-block;

        &:hover {
            cursor: pointer;
            background-color: white;
            color: #048383;
        }
    }
</style>