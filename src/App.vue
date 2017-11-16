<template>
    <div id = "app" class = "app">
        <nav-bar></nav-bar>
        <tasks></tasks>
    </div>
</template>

<script>
    import Navbar from './components/Navbar.vue'
    import Tasks from './components/Tasks.vue'
    export default {
        data() {
            return {}
        },
        components:{
            'nav-bar' : Navbar,
            'tasks' : Tasks
        }
    }
</script>

<style lang = "scss">

</style>
