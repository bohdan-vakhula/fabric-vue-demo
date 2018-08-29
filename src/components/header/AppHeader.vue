<template>
  <div class="header">
    <div class="mode-container">
      <div class="mode-text">
        <span :class="{'on': !isAdvancedMode}">BASIC</span>/<span :class="{'on': isAdvancedMode}">ADVANCED</span>
      </div>
      <switches v-model="isAdvancedMode"></switches>
    </div>
    <div class="preview-save">
      <button class="preview-button"/>
      <button class="save-button"/>
    </div>
  </div>
</template>

<script>
import Switches from 'vue-switches';
export default {
  name: "AppHeader",
  components: {
    Switches
  },
  data: function() {
    return {
      isAdvancedMode: true
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .header {
    display: flex;
    align-items: center;
    width: 100%;
    background: white;
    height: 52px;
    .mode-container {
      display: flex;
      align-items: center;
      margin-left: 70px;
      .mode-text {
        margin-right: 15px;
        color: #ddd;
        .on {
          color: black;
        }
      }
    }
    .preview-save {
      display: flex;
      align-items: center;
      position: absolute;
      left: 50%;
      transform: translate(-50%, 0);
      .preview-button {
        border: none;
        width: 44px;
        height: 36px;
        background: url(../../assets/preview.png);
        cursor: pointer;
        &:focus {
          outline: none;
        }
      }
      .save-button {
        border: none;
        width: 36px;
        margin-left: 15px;
        height: 36px;
        background: url(../../assets/save.png);
        cursor: pointer;
        &:focus {
          outline: none;
        }
      }
    }
  }
</style>
