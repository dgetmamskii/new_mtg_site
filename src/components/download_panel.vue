<template>
    <div className="panel">
        <div v-if="showMain" style = "height: 50vh; display: grid; place-items: center;">
            <button className="button" @click="hideMainButton">Скачать приложение</button>
        </div>
        <div v-if="!showMain">
            <div className="block">
                <div className="inner-block">
                    <input type="email" v-model="name" placeholder="Введите email"  className="email">
                    <h3 className="add-text">*Необязательно. Указанный адрес электронной почты будет использоваться для получения новостей</h3>
                </div>
            </div>
            <div className="block">
                <div className="inner-block">
                    <button className="button" @click="downloadAPK"><a href="/attachments/apk/app-release.apk" download="app-release.apk">Скачать APK</a></button>
                    <h3 className="add-text">Текущая версия: 0.1</h3>
                    <h3 className="add-text">Минимальные системные требования: Android 6.0</h3>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>

export default {
  data () {
    return {
        email : '',
        showMain : true
    }
  },
  props : {
    downloadAPK : {
      type : Function
    }
  },
  methods : {
    hideMainButton () {
        this.showMain = false;
    }
  }
}
</script>
  
<style scoped>
.panel {
    height: 50vh;
    position: relative;
    background-color: rgba(0, 0, 0, 0.5);
}

.button {
    appearance: none;
    border: 0;
    border-radius: 40px;
    background: #ffffff;
    color: #000000;
    padding: 20px 50px;
    font-size: 30px;
    font-weight: 700;
}

.block {
    height: 50vh;
    width: 47vw;
    display: inline-block;
    position: relative;
}

.inner-block {
    position: relative;
    top: 15vh; 
    display: grid; 
    place-items: center;
}

.email {
    appearance: none;
    border: 0;
    border-radius: 40px;
    background: #ffffff;
    color: #000000;
    padding: 20px 50px;
    font-size: 30px;
    font-weight: 700;
    text-align: center;
}

.add-text {
    color: #ffffff;
    font-size: 15px;
    text-align: center;
}
</style>