<template>
    <div className="menu">
        <p>{{ this.element.name }}</p>
    </div>
    <button @click="deleteElem(index)">Удалить</button>
</template>
  
<script>
export default {
  props : {
    element : {
      type : Object,
      Required : true
    },
    index : {
      type : Number,
      Required : true
    },
    deleteElem : {
      type : Function
    }
  },
  methods : {
  }
}
</script>
  
<style scoped>
.menu {
  color: rgb(145, 0, 0);
}
</style>
  