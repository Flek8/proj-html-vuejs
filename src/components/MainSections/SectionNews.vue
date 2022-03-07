<template>
    <section>
        <div class="content">
            <div class="top">
                <h5>OUR EDITORIAL CONTENT</h5>
                <h2>Latest <span class="boxed-text">News</span></h2>
                <p>Every week we publish content about what is best in the business world.</p>
                <MyButton id="btn" :msg="'SEE ALL'"/>
            </div>

            <div class="bottom">
                <MyThumbnail v-for="(el,index) in thumbs" :key="index"
                             :photo="el.photo" :text="el.text" />
            </div>
        </div>
    </section>
</template>

<script>

import MyThumbnail from '../partials/MyThumbnail.vue'

export default {
    name: 'SectionNews',
    components: {
        MyThumbnail
    },
    data() {
        return {
            thumbs: [
                {
                    photo: '1',
                    text: 'Increasing creativity is possible for everyone'
                },
                {
                    photo: '2',
                    text: 'Because market research is part of the business plan'
                },
                {
                    photo: '3',
                    text: 'Working from home is now a trend'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    section {
        padding: 60px 0;
    }
    .content  {
        width: 70%;
        margin: auto;

        .top {
            position: relative;

            span {
                color: #048383;
            }

            #btn {
                position: absolute;
                right: 0;
                bottom: 15px;
            }

            p {
                width: 70%;
                display: inline-block;
            }
        }

        .bottom {
            display: flex;
            justify-content: space-between;
        }
    }
</style>