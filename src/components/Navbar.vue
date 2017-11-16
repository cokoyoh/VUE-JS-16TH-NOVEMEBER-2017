<template>
    <div class = "my-nav-bar" id = "class">
        <div class="top-bar">
            <div class="top-bar-left">
                <ul class="dropdown menu" data-dropdown-menu>
                    <li class="menu-text">To Do List</li>
                    <li><a href="#">Tasks</a></li>
                    <li><a href="#">Add Task</a></li>
                    <li><a href="#">View Task</a></li>
                </ul>
            </div>
            <div class="top-bar-right">
                <ul class="menu">
                    <li><input type="search" placeholder="Search"></li>
                    <li><button type="button" class="button">Search</button></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return{

            }
        }
    }

</script>

<style type = "scss">

</style>