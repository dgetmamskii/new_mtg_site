<template>
    <div className="panel">
      <div className="header">
        <h1><b>Скриншоты</b></h1>
      </div>
      <div className="image_panel">
        <div className="image_block">
          <img :src="pictures[0]">
        </div>
        <div className="image_block">
          <img :src="pictures[1]">
        </div>
        <div className="image_block">
          <img :src="pictures[2]">
        </div>
      </div>
    </div>
</template>
  
<script>
import screenshot_1 from "/src/assets/screenshots/screenshot-1.jpg"
import screenshot_2 from "/src/assets/screenshots/screenshot-2.jpg"
import screenshot_3 from "/src/assets/screenshots/screenshot-3.jpg"
export default {
  data () {
    return {
      pictures : [
        screenshot_1,
        screenshot_2,
        screenshot_3
      ]
    }
  }
}
</script>
  
<style scoped>
.panel {
    height: 100vh;
    position: relative;
    background-color: rgba(0, 255, 255, 0.048);
}


.header {
    color: rgb(255, 255, 255);
    font-size: 40px;
    text-align: center;
    top: 80px;
    bottom : 40px;
    height: 240px;
    position: relative;
}

.image_panel {
    position: relative;
    top : 3vh;
    margin-left : auto;
    margin-right : auto;
    width: 90vw;
    left : 1vw;
    height: 100vh-240px;
}

.image_block {
    position: relative;
    margin-left: 11vw;
    height: auto;
    width: 280px;
    display: inline-block;
    object-fit: contain;
}
</style>