<template>
    <div class="card">
        <img :src="require('../../assets/img/team-' + photo + '.jpg')" :alt="name + ' photo' ">
        <div class="info">
            <h3>{{name}}</h3>
            <h5 class="job">{{job}}</h5>
            <div class="social">
                <span><i class="fa-brands fa-facebook-f"></i></span>
                <span><i class="fa-brands fa-twitter"></i></span>
                <span><i class="fa-brands fa-linkedin-in"></i></span>
                
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
        padding: 10px 0;

        img {
            width: 90px;
            
            border-radius: 5px;
        }

        .info {
            
            padding: 2px 0 5px 15px;
            color: white;

            h3 {
                margin:0 0 5px 0;
                font-size: 26px;
            }

            h5.job {
                color: white;
                text-transform: uppercase;
            }

            .social {
                display: flex;
                color: #048383;
                margin-top: 10px;


                span {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    background-color: #729fa13a;
                    padding: 10px;
                    border-radius: 50%;
                    width: 36px;
                    height: 36px;
                    margin: 3px;
                }
            }
        }
    }

</style>