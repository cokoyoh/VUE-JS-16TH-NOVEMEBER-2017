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
            <h4>Remarks | Vue Conditionals</h4>
            <p v-if="marks.cokoyoh >= 60">Charles scored above average</p>
            <p v-if="marks.shangri_la == 100">I know that place, That is Shangri-La. It's magical</p>
        </div>

        <div class="event-handling">
            <button type="button" @click="onSubmitButton">Please Click Me</button>
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
                    'shangri_la': 100
                }
            }
        },
        methods:{
            onSubmitButton(){
                let what_now = "Learning Vue? You must be a genius!"
                alert(what_now)
                console.log("Mmh! ",what_now)
            }
        }
    }
</script>

<style lang = "scss">

</style>
