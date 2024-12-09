<template>
    <div className="panel" v-if="this.isShow">
        <div className="button">
            <button @click="toggle_panel_visibility">{{ this.buttonName }}</button>
        </div>
        <div className="element">
            <div className="block">Краткое описание</div>
            <div className="block">Скриншоты</div>
            <div className="block">Скачать</div>
        </div>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            buttonClass : "buttonHide",
            buttonName : "Скрыть панель",
            isShow : true,
        }
    },
    methods: {
        changeButton() {
            if (this.buttonClass == "buttonShow"){
                this.buttonClass = "buttonHide";
                this.buttonName = "Показать панель";
            } else {
                this.buttonClass = "buttonShow"
                this.buttonName = "Скрыть панель";
            }
        },
        toggle_panel_visibility() {
            this.isShow = !this.isShow
        }
    }  
}
</script>
  
<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Anticva';
  
}

.panel {
  color: rgb(255, 255, 255);
  font-size: 30px;
  text-align: center;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 260px;
  background: #11101d;
  align-items: center;
  visibility: hidden;
}

.block {
    color: rgb(255, 255, 255);
    font-size: 30px;
    width: 100%;  
    top: 20%;
    padding-top: 50%;
}

.element {
    color: rgb(255, 255, 255);
    font-size: 30px;
    height: 600px;
    width: 100%;
    align-items: center;
    text-align: center;    
    position: relative;
    top: 15%;
}

.button {
    color: rgb(255, 255, 255);
    font-size: 30px;
    height: 40px;
    width: 100%;
    align-items: center;
    text-align: center;    
    position: absolute;
    top: 15%;
}

</style>