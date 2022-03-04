<template>
    <section>
        <div class="sect-left">
            <h5>ABOUT THE NETWORK</h5>
            <h2><span class="boxed-text">The</span> Company</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras iaculis diam varius diam ultricies lacinia. Mauris lacus tellus, ultrices eu voluptat sit amet, finibus a ipsum.</p>
            <p>Curabitur convallis, diam a egestas iaculis, neque lorem interdum felis, in viverra lacus tortor in leo.</p>
        </div>

        <div class="sect-right">
            <MyBox class="box" v-for="(el,index) in titles" :key="index" :icon="el.icon" :text="text" :title="el.word" />
        </div>
    </section>
</template>

<script>
import MyBox from '../partials/MyBox.vue'

export default {
    name: 'SectionCompany',
    components: {
        MyBox
    },
    data() {
        return {
            text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit',
            titles: [
                {
                    icon:'fa-award',
                    word:'Tradition'
                },
                {
                    icon:'fa-lock',
                    word:'Security'
                },
                {
                    icon:'fa-pen-to-square',
                    word:'Certificate'
                },
                {
                    icon:'fa-graduation-cap',
                    word:'Expertise'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    section {
        color: white;
        background-color: black;
        padding: 70px 15%;

        &::after {
            content: '';
            display: table;
            clear: both;
        }

        h5 {
            color: #048383;
        }

        h2 {
            margin: 15px 0;
            font-size: 50px;
        }

        p {
            margin-bottom: 15px;
            font-size: 16px;
        }

        .sect-left, .sect-right {
            float: left;
            width: 50%;
        }

        .sect-left {
            padding-right: 30px;
        }

        .sect-right {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-content: space-around;

            .box {
                width: 50%;
                margin-top: 32px;
            }
        }
    }
</style>