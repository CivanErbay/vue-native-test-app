<template>
  <view class="container">
    <image class="tamagotchi" :source="require('./assets/tamagotchi.png')" />

 
      <text-input
        :style="{
          margin: 20,
          height: 60,
          width: 150,
          borderColor: 'black',
          borderWidth: 3,
        }"
        v-model="task"
      />


    <text @press="addTask" class="task">Add</text>
    <view class="task-list">
      <text v-for="task in taskList" :key="task">
        {{ task }}
      </text>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      task: "",
      taskList: [],
    };
  },
  methods: {
    addTask() {
      this.taskList.push(this.task);
      this.task = ''
    },
  },
};
</script>

<style>
.container {
  flex: 1;
  align-items: center;
  justify-content: flex-start;
  background-color: rgb(187,187,187);
}
.tamagotchi {
  height: 300;
  width: 300;
  margin-top: 30;
}
.task-wrapper {
  align-items: center;
  justify-content: center;
  flex-direction: row;
  padding-top: 30;
}
.task {
  font-size: 30;
  font-weight: bold;
}
</style>