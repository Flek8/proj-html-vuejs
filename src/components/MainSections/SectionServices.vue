<template>
    <section>
        <div class="content">
            <div class="top">
                <h5>OUR BUSINESS AREAS</h5>
                <h2>Excellence in <span class="boxed-text">Services</span></h2>
                <p>We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.</p>
                <MyButton id="btn" :msg="'SEE ALL'"/>
            </div>

            <div class="bottom">
                <MyBox v-for="(el,index) in titles" :key="index"
                        :iconTop="el.iconTop" :iconArrow="'fa-arrow-right'"
                        :title="el.words" :text="text"
                        class="box" />
            </div>
        </div>
    </section>
</template>


<script>
import MyButton from '../partials/MyButton.vue';
import MyBox from '../partials/MyBox.vue';

export default {
    name: 'SectionServices',
    components: {
        MyButton,
        MyBox
    },
    data() {
        return {
            text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
            titles: [
                {
                    iconTop: 'fa-network-wired',
                    words: 'Audit & Assurance'
                },
                {
                    iconTop: 'fa-briefcase',
                    words: 'Financial Advisory'
                },
                {
                    iconTop: 'fa-chart-simple',
                    words: 'Analytics and M&A'
                },
                {
                    iconTop: 'fa-plane',
                    words: 'Middle Marketing'
                },
                {
                    iconTop: 'fa-globe-stand',
                    words: 'Legal Consulting'
                },
                {
                    iconTop: 'fa-inbox',
                    words: 'Regulatory Risk'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    section {
        width: 100%;
        padding: 80px 0;
        background-color: #e8ecea;
        
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
                flex-wrap: wrap;
                justify-content: space-between;

                .box {
                    width: calc((100% - 40px) / 3);
                    background-color: white;
                    border-radius: 5px;
                    padding: 20px;
                    margin-bottom: 20px;

                }
            }
        }
    }
    
</style>