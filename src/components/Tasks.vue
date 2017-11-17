<template>
    <div class = "tasks" id = "tasks">
        <div class = "grid-container">
            <div class = "large-8 large-offset-2 columns">
                <h4>ToDo List</h4>
                <div class = "panel callout radius">
                    <div class = "row">
                        <div class = "large-3 medium-3 columns"><strong>Task Title</strong></div>
                        <div class = "large-3 medium-3 columns"><strong>Body</strong></div>
                        <div class = "large-3 medium-3 columns"><strong>Date</strong></div>
                        <div class = "large-3 medium-3 columns"><strong>Status</strong></div>
                    </div>
                    <div class = "row" v-for = "task in tasks">
                        <div class = "large-3 medium-3 columns">{{task.title}}</div>
                        <div class = "large-3 medium-3 columns">{{task.description}}</div>
                        <div class = "large-3 medium-3 columns">{{task.date}}</div>
                        <div class = "large-3 medium-3 columns">{{task.status}}</div>
                    </div>
                    <hr>
                    <form>
                        <div class = "row">
                            <div class = "large-6 medium-6 columns">
                                <div class = "row">
                                    <label>Task
                                        <input type = "text" placeholder = "Title of the task..."
                                               v-model = "title"/>
                                    </label>
                                </div>
                                <div class = "row">
                                    <label>Description
                                        <textarea placeholder = "What do you want to do?" rows = "5"
                                                  v-model = "description"></textarea>
                                    </label>
                                </div>
                            </div>
                            <div class = "large-6 medium-6 columns">
                                <div class = "row">
                                    <label>Date
                                        <input type = "date" placeholder = "Pick date" v-model = "date">
                                    </label>
                                </div>
                                <div class = "row">
                                    <label>Status
                                        <select v-model = "status">
                                            <option value = "incomplete" selected>Incomplete</option>
                                            <option value = "completed">Completed</option>
                                        </select>
                                    </label>
                                </div>
                                <div class = "row">
                                    <div class = "button success expand" type = "submit" @click = 'addNewTask'>
                                        Add Task
                                    </div>
                                </div>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                title: '', description: '', date: '', status: '',
                tasks: [
                    {'title': '', 'description': '', 'date': '', 'status': ''},
                ]
            }
        },
        methods: {
            addNewTask: function (e) {
                e.preventDefault();
                console.log("method called here");
                this.tasks.unshift({
                    title: this.title,
                    description: this.description,
                    date: this.date,
                    status: this.status,
                });
                this.title = '';
                this.description ='';
                this.status = '';
                this.date =''
            }
        }
    }

</script>

<style type = "scss">
    .tasks {
        padding: 30px 0 30px;
    }
</style>