<template>
  <div class="wrapper">
    <div
      class="modal"
      v-dragscroll
    >
      <div class="content"></div>
    </div>
    <button
      class="close"
      @click="$emit('close')"
    >
        X
      </button>
  </div>
</template>

<script>
export default {
  name: 'appModal',

}
</script>

<style lang="sass" scoped>
.wrapper
  width: 500px
  height: 500px
  position: relative

.modal
  width: 500px
  height: 500px
  overflow: hidden
  cursor: grab
  &:active
    cursor: grabbing

.content
  width: 1020px
  height: 780px
  background: url('../static/MJ.jpeg')

</style>
