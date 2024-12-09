<template>
    <div className="panel">
      <div className="header">
        <h1><b>MTG Organizer</b></h1>
      </div>
      <div className="info">
        <p>Добро пожаловать в MTG Organizer — идеальное приложение для всех поклонников и коллекционеров Magic: The Gathering (MTG)! Наше приложение создано для того, чтобы помочь вам организовать и управлять вашей коллекцией карт.</p>
        <p>С MTG Organizer ваша коллекция карт и игровые сессии всегда будут под контролем. Скачайте приложение сейчас и начните организовывать свою MTG-вселенную с максимальным удобством!</p>
      </div>
    </div>
</template>
  
<script>
export default {
}
</script>
  
<style scoped>
.panel {
  height: 100vh;
  position: relative;
}

.header {
  color: rgb(255, 255, 255);
  font-size: 40px;
  text-align: center;
  position: relative;
  top: 180px;
}

.info {
  color: rgb(255, 255, 255);
  width: 50%;
  top: 380px;
  left: 25%;
  position: relative;
  font-size: 20px;
  text-align: center;
}
</style>