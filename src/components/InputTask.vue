<template>
  <div>
      <input placeholder="O que precisa ser feito?" class="new-todo" v-on:keyup.enter="addTask">
  </div>
</template>

<script>
import { Task } from "../models/Task";

export default {

  data() {
    return {

    }
  },
    methods: {
      addTask($event){
        let task = new Task()
        task.completed = true
        task.title = $event.target.value
        console.log(task)
      }
    }
}


</script>

<style>

</style>