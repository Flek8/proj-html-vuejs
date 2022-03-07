<template>
    <footer>
        <div class="container">
            <div class="top">
                <div class="infos">
                    <img src="../assets/img/nexgen-logo.svg" alt="NEXGEN logo" height="40">
                    <p>A Functional HTML Template for Corporate & Business</p>
                    <span><i class="fa-solid fa-phone"></i> +1(305)1234-5678</span>
                    <span><i class="fa-solid fa-envelope"></i> hello@example.com</span>
                    <span><i class="fa-solid fa-location-dot"></i> Main Avenue, 987</span>
                    <MyButton class="btn-black" :msg="'GET IN TOUCH'"/>
                </div>
                <MyList v-for="(el,index) in lists" :key="index"
                        :title="el.name" :list="el.items" />
                
            </div>
        </div>

            <div class="bottom">
                <div>
                    <span>Enjoy the low price. We are tracking any intention of piracy.</span>
                </div>
                <div>
                    <span>2020 NEXGEN is Proudly Powered by <span class="green">Codings</span>.</span>
                </div>
                <div id="to-header">
                    <a href="#app"><i class="fa-solid fa-arrow-up"></i></a>
                </div>
            </div>
        
        
    </footer>
</template>

<script>

import MyList from './partials/MyList.vue';
import MyButton from './partials/MyButton.vue';

export default {
    name: 'MyFooter',
    components: {
        MyList,
        MyButton
    },
    props: {
        lists: Array
    }
}
</script>

<style scoped lang='scss'>
    footer {
        background-color: #0c0f0f;
        color: gray;

        .container {
            width: 70%;
            margin: auto;

            .top {
                display: flex;
                justify-content: space-between;
                padding: 60px 0;

                .infos {
                    width: calc((100% - 60px)/4);
                    img {
                        margin-bottom: 10px;
                    }

                    span {
                        display: block;
                        margin-bottom: 15px;
                    }

                    .btn-black {
                        background-color: #0c0f0f;
                        margin-top: 10px;
                    }
                }
            }

        }
        
        .bottom {
            display: flex;
            justify-content: space-between;
            background-color: black;
            padding: 25px 15%;
            color: gray;
            font-size: 14px;
            position: relative;

            .green {
                color: #048383;
            }

            #to-header {
                display: inline-block;
                position: absolute;
                right: 15px;
                bottom: 15px;
                background-color: #161a1b;
                width: 40px;
                height: 40px;
                border-radius: 50%;
                display: flex;
                justify-content: center;
                align-items: center;

                &:hover {
                    cursor: pointer;
                }

                a {
                    text-decoration: none;
                    color: black;
                }
            }
        }
        
    }
</style>