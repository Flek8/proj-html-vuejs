<template>
    <section>
        <div class="container">
            <div class="left">
                <h5>WE LIKE WHAT WE DO</h5>
                <h2><span class="boxed-text">Team</span> of Experts</h2>
                <p>Ethics and integrity are the bases on which our professionals build their careers. They are fundamentals that become daily attitudes.</p>
                <div class="staff">
                    <MyCard />
                </div>
            </div>

            <div class="right">

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
                    job: 'cto & co-founder'
                },
                {
                    name: 'David Cooper',
                    job: 'cto & co-founder'
                },
                {
                    name: 'David Cooper',
                    job: 'cto & co-founder'
                },
                {
                    name: 'David Cooper',
                    job: 'cto & co-founder'
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

            .left {
                width: 60%;
                float: left;

                h2 {
                    color: white;
                }
            }

            .right {
                width: 40%;
                float: left;
            }
        }
    }

</style>