<template>
  <div class="debug-mode" @click="displayDebug">
    Debug mode
  </div>
</template>

<script lang="ts">
const { remote } = require('electron');
const { BrowserWindow } = remote;

const debugWindow = BrowserWindow.getAllWindows()[0];

export default {
  name: 'debug-mode',
  methods: {
    displayDebug() {
      debugWindow.show();
    },
  },
};
</script>

<style lang="scss" scoped>
.debug-mode {
  position: absolute;
  right: 15px;
  bottom: 15px;
  font-size: 12px;
  cursor: pointer;
}
</style>
