<template>
    <section>

        <div class="top">
            <h5>HOW IT WORKS IN PRACTICE</h5>
            <h2><span class="boxed-text">Process</span> Management</h2>
            <p>We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned</p>
        </div>

        <div class="bottom">
            <div v-for="(el,index) in numeri" :key="index" class="number">
                <span>0{{el}}</span>
            </div>
            

            <MyBox v-for="(el,index) in titles" :key="index"
                    :title="el" :text="text"
                    class="box"
            />
            
        </div>
        <div id="line"></div>
    </section>
</template>

<script>

import MyBox from '../partials/MyBox.vue'

export default {
    name: 'SectionManagement',
    components: {
        MyBox
    },
    data() {
        return {
            numeri: [1,2,3,4,5],
            text: 'Lorem ipsum dolor sit amet consectetur',
            titles: ['Collection of information',
                     'Strategic planning',
                     'Assignment of responsabilities',
                     'Formatting process',
                     'Continuity formalization']
        }
    },
    
}
</script>

<style scoped lang="scss">
    section {
        padding: 80px 0;
        text-align: center;
        position: relative;

        .top {
            width: 50%;
            margin: auto;

            span {
                color: #048383;
            }
        }

        .bottom {
            width: 80%;
            margin: auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;

            .number {
                display: inline-block;
                width: 20%;
                display: flex;
                justify-content: center;
                z-index: 9;

                span {
                    width: 40px;
                    height: 40px;
                    text-align: center;
                    padding: 5px;
                    background-color: #d9f1f1;
                    color: #048383;
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    font-weight: bold;
                }
            }

            .box {
                width: 20%;
                padding: 0 25px;
            }

        }

        #line {
            width: 100%;
            height: 4px;
            background-color: #d9f1f1;
            position: absolute;
            top: 252px;
        }
        
    }
</style>