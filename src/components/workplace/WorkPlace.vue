<template>
  <div class="workplace">
    <Worksheet/>
    <EditToolbox/>
  </div>
</template>

<script>
import Worksheet from "./Worksheet.vue";
import EditToolbox from "./toolbox/EditToolbox.vue";

export default {
  name: "WorkPlace",
  components: {
    Worksheet,
    EditToolbox
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .workplace {
    flex: 1;
    position: relative;
  }
</style>
