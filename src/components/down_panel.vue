<template>
    <div className="panel">
        <div className="block">
            <div className="block-text" @click="openModal('Лицензионное соглашение')">
                <text>Лицензионное соглашение</text>
            </div>         
            <div className="block-text" @click="openModal('Политика конфиденциальности')">
                <text>Политика конфиденциальности</text>
            </div>
        </div>
    </div>
    <ModalWindow ref="modalWindow"/>
</template>
  
<script>
import ModalWindow from './modal_window.vue'

export default {
    components : { ModalWindow },
    data () {
        return {
        }
    },
    methods : {
        openModal(title) {
            this.$refs.modalWindow.openModal(title)
        }
    }
}
</script>
  
<style scoped>
.panel {
    border-top: 3px;
    border-color: white;
    border: solid;
    height: 20vh;
    position: relative;
    background-color: rgb(0, 0, 0);
}
.block {
    height: 10vh;
    width: 25vw;
    top: 5vh;
    left: 3vw;
    position: relative;
}

.block-text {
    position: relative;
    background-color: rgb(0, 0, 0);
    margin-top: 10px;
    color: white;
    display: block;
    font-style: normal;
    cursor: pointer;
}

</style>