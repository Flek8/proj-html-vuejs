<template>
    <section>
        <div class="container">
            <div class="left">
                <h5>NEWSLETTER</h5>
                <h2><span class="boxed-text-dark">Know</span> First</h2>
                <p>Follow closely and receive content about our company and the news of the current market.</p>
            </div>

            <div class="right">
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <MyButton id="btn" :msg="'SUBSCRIBE'"/>
            </div>
        </div>
    </section>
</template>

<script>

import MyButton from '../partials/MyButton.vue'

export default {
    name: 'NewsLetter',
    components: {
        MyButton
    }
}
</script>

<style scoped lang="scss">
    section {
        background-image: url(../../assets/img/bg-1.jpg);
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        padding: 70px 0;

        .container {
            width: 62%;
            margin: auto;

            &::after {
                content: '';
                display: table;
                clear: both;
            }

            .left, .right {
                width: 50%;
                float: left;
                
            }

            .left {
                h2 {
                    color: white;
                }
            }

            .right {

                padding: 0 20px;

                input {
                    width: 80%;
                    padding: 12px;
                    background-color: rgba(179, 179, 179, 0.432);
                    border: none;
                    border-radius: 5px;
                    margin-bottom: 15px;
                    
                }
            }
        }
    }
</style>