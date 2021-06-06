<template>
  <view class="container">
    <text class="text-color-primary">{{ message }}</text>
    <button title="hannaaaaaaa" @press="exclaim" />
  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello my Name is",
      messageArray: ['',' Hanna ',' and ',' Civan ', 'and'],
      messageCounter: 0
    };
  },
  methods: {
    exclaim() {
      if(this.messageCounter < 4) this.messageCounter += 1;
      this.message += this.messageArray[this.messageCounter]
    }
  },
};
</script>

<style>
.container {
  flex: 1;
  background-color: green;
  align-items: center;
  justify-content: center;
}
.text-color-primary {
  color: black;
  font-size: 30;
}
</style>