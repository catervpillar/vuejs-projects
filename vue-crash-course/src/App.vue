<script setup>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
</script>

<template>
  <div class="container">
    <Header title="Task Tracker" />
    <Tasks :tasks="tasks" />
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
    Header,
    Tasks
  },
  data() {
    return {
      tasks: []
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: "Doctors Appointment",
        day: "March 1st at 2:30pm",
        reminder: true
      },
      {
        id: 2,
        text: "Pizza Night",
        day: "March 7st at 8:30pm",
        reminder: true
      },
      {
        id: 3,
        text: "Food Shopping",
        day: "March 3st at 10:00am",
        reminder: true
      }
    ]
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Poppins', sans-serif;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

h1 {
  font-weight: 500;
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
</style>
