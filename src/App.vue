<template>
    <div id = "app" class = "app">
        <input type = "text" id = "input" v-model = "message">
        <p>The value of this input is {{message}}</p>

        <div class = "interns">
            <h4>The Interns Names are</h4>
            <ul v-for="intern in interns.names">
                <li>{{intern}}</li>
            </ul>
        </div>

        <div class="conditionals">

        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                message: "Welcome to vue Charles",

                interns: {
                    names: ['charles', 'salome', 'the nyamu', 'caro', 'kabiru', 'douglas', 'maina', 'mwiti']
                },

                marks:{
                    'cokoyoh': 78,
                    'yoda': 99,
                    'shangri-La': 100
                }
            }
        }
    }
</script>

<style lang = "scss">

</style>
