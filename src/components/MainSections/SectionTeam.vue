<template>
    <section>
        <div class="container">
            <div class="left">
                <h5>WE LIKE WHAT WE DO</h5>
                <h2><span class="boxed-text-dark">Team</span> of Experts</h2>
                <p>Ethics and integrity are the bases on which our professionals build their careers. They are fundamentals that become daily attitudes.</p>
                <div class="staff">
                    <MyCard v-for="(el,index) in staff" :key="index"
                            :job="el.job" :name="el.name" :photo="el.photo" />
                </div>
            </div>

            <div class="right">
                <h4>President Speech</h4>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut lacinis diam.</p>
                <p>Vivamus efficitur et est quis posuere. Nulla sollicitudin vulputate dui, id pretium tortor congue eu. Integer aliquet justo eu quam voluptat ullamcorper.</p>
                <p>Duis ut hendrerit mauris Phasellus faucibus ut enim vel tincidunt. Nunc venenatis a dui et laoreet.</p>
                <span>T. Johnson</span>
                <div id="quote-icon"><i class="fa-solid fa-quote-right"></i></div>
            </div>
        </div>
        
    </section>
</template>

<script>

import MyCard from '../partials/MyCard.vue'

export default {
    name: 'SectionTeam',
    components: {
        MyCard
    },
    data() {
        return {
            staff: [
                {
                    name: 'David Cooper',
                    job: 'cto & co-founder',
                    photo: '1'
                },
                {
                    name: 'Oliver Jones',
                    job: 'chief procurement',
                    photo: '3'
                },
                {
                    name: 'Emma Lopez',
                    job: 'chief marketing',
                    photo: '2'
                },
                {
                    name: 'T. Johnson',
                    job: 'ceo & president',
                    photo: '4'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

    section {
        background-color: black;

        &::after {
            content: '';
            display: table;
            clear: both;
        }

        .container {
            width: 70%;
            margin: auto;
            padding: 60px 0;

            .left {
                width: 60%;
                float: left;

                h2 {
                    color: white;
                }

                .staff {
                    display: flex;
                    flex-wrap: wrap;
                }
            }

            .right {
                width: 30%;
                float: right;
                margin-top: 38px;
                padding: 20px;
                background-color: #048383;
                border-radius: 5px;
                position: relative;

                h4 {
                    color: white;
                    font-size: 20px;
                }

                p {
                    margin: 20px 0;
                    color: white;
                }

                span {
                    font-weight: bold;
                    color: white;
                }

                #quote-icon {
                    display: inline-block;
                    position: absolute;
                    bottom: 10px;
                    right: 15px;
                    color: rgb(90, 90, 90);
                    font-size: 26px;
                }
            }
        }
    }

</style>