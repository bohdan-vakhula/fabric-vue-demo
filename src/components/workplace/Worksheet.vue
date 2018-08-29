<template>
  <div class="worksheet">
    <canvas id="canvas"/>
  </div>
</template>

<script>
import { fabric } from 'fabric';
export default {
  name: "Worksheet",
  mounted: function() {
    let canvas = new fabric.Canvas('canvas', {
      backgroundColor: 'white',
      selectionColor: 'blue',
      selectionLineWidth: 2,
      width: 1024,
      height: 600
    });
    let rect = new fabric.Rect({
      left: 400,
      top: 200,
      fill: 'red',
      width: 100,
      height: 100
    });
    canvas.add(rect);
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .worksheet {
    width: 1024px;
    height: 600px;
    background: white;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
</style>
