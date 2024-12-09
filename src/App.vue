<template>
  <SidePanel />
  <Header />
  <Screenshots />
  <DownloadPanel :downloadAPK="downloadAPK"/>
  <DownPanel />
  <ModalWindow ref="modalWindow"/>
</template>

<script>
// import axios from 'axios';

import Header from './components/short_info.vue'
import SidePanel from './components/side_panel.vue'
import Screenshots from './components/screen_shots.vue'
import DownloadPanel from './components/download_panel.vue'
import DownPanel from './components/down_panel.vue'
import ModalWindow from './components/modal_window.vue'

export default {
  components : { Header, SidePanel, Screenshots, DownloadPanel, DownPanel, ModalWindow},
  data() {
    return {
    }
  },
  methods: {
    downloadAPK () {
      try {
        console.log('LOG_DOWNLOAD_STARTED');
        this.$refs.modalWindow.openModal("Загрузка началась")
      } catch (error) {
        console.log('LOG_DOWNLOAD_ERROR:', error);
      }
    }
  }
}
</script>

<style scoped>
h3 {
  font-size: larger;
}

p {
  color: rgb(145, 0, 0);
}

.menu {
  color: rgb(145, 0, 0);
}

.header {
  text-align: center;
}
</style>
