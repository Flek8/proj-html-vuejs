<template>
    <div>
        <h4>{{title}}</h4>
        <ul>
            <li  v-for="(el,index) in list" :key="index">
                <i class="fa-solid fa-chevron-right"></i> {{el}}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'MyList',
    props: {
        title: String,
        list: Array
    }
}
</script>

<style scoped lang="scss">
    div {
        width: calc((100% - 60px)/4);
        background-color: #161a1b;
        padding: 25px;
        border-radius: 10px;

        h4 {
            color: white;
            margin-bottom: 15px;
        }

        li {
            list-style: none;
            margin: 5px 0;
            padding: 2px 0;
            &:hover {
                color: white;
                cursor: pointer;
            }
        }

    }
</style>