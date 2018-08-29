<template>
  <div class="sidebar">
    <div class="item-list">
      <div class="menu-item search"></div>
      <div class="menu-item list"></div>
      <div class="menu-item images"></div>
      <div class="menu-item text"></div>
      <div class="menu-item shape"></div>
    </div>
    <div class="fill-space"></div>
    <div class="help-menu-item"></div>
  </div>
</template>

<script>
export default {
  name: "SideBar"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .sidebar {
    background: #4d4d4d;
    width: 72px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .item-list {
      .menu-item {
        border-bottom: 1px solid #979797;
        border-right: 1px solid #979797;
        border-left: 1px solid #979797;
        width: 70px;
        height: 70px;
        cursor: pointer;
        &.search {
          background: url('../../assets/search.png');
        }
        &.list {
          background: url('../../assets/list.png');
        }
        &.images {
          background: url('../../assets/images.png');
        }
        &.text {
          background: url('../../assets/text.png');
        }
        &.shape {
          background: url('../../assets/shape.png');
        }
      }
    }
    .fill-space {
      flex: 1;
      border: 1px solid #979797;
    }
    .help-menu-item {
      border: 1px solid #979797;
      width: 70px;
      height: 70px;
      cursor: pointer;
      background: url('../../assets/question.png');
    }
  }
</style>
