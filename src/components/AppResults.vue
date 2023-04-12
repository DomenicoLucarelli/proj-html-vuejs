<script>
export default {
    name:'AppResults',
    data() {
        return {
            results: [
                {
                    num: 128,
                    text: 'Certifications'
                },

                {
                    num: 230,
                    text: 'Employees'
                },

                {
                    num: 517,
                    text: 'Customers'
                },

                {
                    num: 94,
                    text: 'Countries Served'
                },
            ]
        }
    },
}
</script>

<template>
    <div class="container">

        <div class="title">
            <h5>What are we doing</h5>
            <h2><mark>Results</mark> in Number</h2>
        </div>

        <div class="results">
            <div class="result" v-for="(result, index) in results" :key="index">
                <span class="data">{{result.num}}</span>
                <span class="info">{{result.text}}</span>
            </div>
        </div>
        
    </div>
</template>

<style lang="scss" scoped >
    .container{
        min-height: 400px;
        background-image: url('img/bg-7.jpg');
        background-size: cover;
        background-position-y: center;

        .title{
            max-width: 900px;
            margin:  auto;
            padding: 100px 0 50px 0;
            text-align: center;

            h5{
                color: #00aaaa;
                padding-bottom: 20px;
                text-transform: uppercase;
            }

            h2{
                color: white;
                font-weight: 800;
            }

            mark{
                background-color: #0d2d2f;
                color: white;
            }

        }

        .results{
            display: flex;
            justify-content: center;
            gap: 50px;
            padding-bottom: 100px;

            .result{
                display: flex;
                flex-direction: column;

                .data{
                    text-align: center;
                    color: #00aaaa;
                    font-size: 2em;
                    font-weight: bold;
                }

                .info{
                    color: white;
                    font-size: 1.5em;
                    font-weight: bold;
                }
            }
        }
    }
</style>