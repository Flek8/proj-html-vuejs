<template>
    <header>
        <div class="header-top">
            <div>
                <span><i class="fa-solid fa-clock"></i> Open Hours:Mon - Sat - 9.00 - 18.00</span>
            </div>
            <div>
                <a href="#"><span><i class="fa-solid fa-phone"></i> +1(305)1234-5678</span></a>
                <a href="#"><span><i class="fa-solid fa-envelope"></i> hello@example.com</span></a>
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
            </div>
        </div>
        <div class="header-bottom">
            <nav>
                <img src="../assets/img/nexgen-logo.svg" alt=" logo nexgen" height="40">
                <ul>
                    <li v-for="(el,index) in menuList" :key="index"><a href="#">{{el}}</a></li>
                    
                    <li><a href="#"><MyButton :msg="'GET IN TOUCH'" /> </a></li>
                </ul>
            </nav>

            <div class="jumbotron">
                <div class="content">
                    <h5>FUSIONS & ACQUISITIONS</h5>
                    <h1>Insurance Consulting</h1>
                    <input type="text" placeholder="Name">
                    <input type="text" placeholder="Email">
                    <input type="text" placeholder="Phone">
                    <select name="" id="">
                        <option value="default">More Info</option>    
                    </select>
                    <MyButton :msg="'GET IN TOUCH'" />
                    <MyButton class="btn-white" :msg="'READ MORE'" />
                </div>
            </div>
        </div>
    </header>
</template>

<script>
import MyButton from './partials/MyButton.vue'
export default {
    name: 'MyHeader',
    components: {
        MyButton
    },
    props: {
        menuList: {
            Array
        }
    }
}
</script>

<style scoped lang='scss'>
    header {
        .header-top {
            display: flex;
            justify-content: space-between;
            background-color: #2f4f55;
            padding: 10px 16%;
            color: gray;

            
        }

        .header-bottom {
            background-image: url(../assets/img/bg-6.jpg);
            background-size: cover;
            background-repeat: no-repeat;
            background-position-y: -50px;


            nav {
                width: 70%;
                margin: auto;
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 10px;

                li {
                    display: inline-block;
                    color: black;
                }
            }

            
        }

        .btn-white {
            background-color: white;
            color: #048383;
            margin-left: 10px;

            &:hover {
                background-color: #048383;
                color: white;
            }
        }

        a {
            text-decoration: none;
            margin: 10px;
            color: inherit;
            font-size: 14px;
        }

        .jumbotron {
            width: 70%;
            margin: auto;
            &::after {
                content: '';
                display: table;
                clear: both;
            }

            .content {
                float: right;
                width: 45%;
                padding: 100px 0;

                h1 {
                    font-size: 70px;
                    font-weight: bold;
                    margin-bottom: 30px;

                }

                h5 {
                    color: #048383;
                }

                input {
                    border: none;
                    border-radius: 3px;
                    background-color: #aeb0b0;
                    padding: 10px;
                    margin: 0px 10px 10px 0;
                }

                select {
                    border: none;
                    border-radius: 3px;
                    background-color: #aeb0b0;
                    padding: 10px;
                    color: rgb(121, 121, 121);
                    width: 182px;
                }
            }

            
        }
    }
</style>