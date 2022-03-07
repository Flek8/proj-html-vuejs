<template>
    <div class="card">
        <img :src="require('../../assets/img/team-' + photo + '.jpg')" :alt="name + ' photo' ">
        <div class="info">
            <h3>{{name}}</h3>
            <h5 class="job">{{job}}</h5>
            <div class="social">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin-in"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyCard',
    props: {
        photo: String,
        name: String,
        job: String
    }
    
}
</script>

<style scoped lang="scss">
    .card {
        width: 50%;
        display: flex;
        align-items: center;

        img {
            width: 60px;
            height: 80px;
            border-radius: 5px;
        }

        .info {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 5px 15px;
            color: white;

            h5.job {
                color: white;
                text-transform: uppercase;
            }

            .social {
                display: flex;

                i {
                    background-color: #729fa13a;
                    height: 20px;
                    width: 20px;
                    border-radius: 50%;
                    color: #048383;
                }
            }
        }
    }

</style>