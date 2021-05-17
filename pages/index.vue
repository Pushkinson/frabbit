<template>
  <main class="container">
    <div class="links">
      <a
        href="#"
        class="button--green"
        @click.prevent="openModal"
      >
        Open modal
      </a>
      <a
        href="#"
        class="button--grey"
        @click.prevent="openDrag"
      >
        Open drag
      </a>
    </div>
    <div
      class="modal__wrapper"
      v-if="isModalOpen"
    >
      <app-modal
        @close="closeModal"
      />
    </div>
    <div
      class="drag"
      v-drag
      v-if="isDragOpen"
    >
      <button
        class="close"
        @click="closeDrag"
      >
        X
      </button>
    </div>
  </main>
</template>

<script>
import appModal from '@/components/appModal.vue';

export default {
  components: { appModal },

  data() {
    return {
      isModalOpen: false,
      isDragOpen: false,
    }
  },

  methods: {
    openModal() {
      this.isModalOpen = true;
    },

    closeModal() {
      this.isModalOpen = false;
    },

    openDrag() {
      this.isDragOpen = true;
    },

    closeDrag() {
      this.isDragOpen = false;
    }
  },
}
</script>

<style lang="sass" scoped>
.container
  margin: 0 auto
  min-height: 100vh
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  text-align: center
  position: relative
  background-color: #E8FAFD
  box-shadow: 0px 8px 48px rgba(0, 0, 0, 0.26)

.title
  font-family: 'Source Sans Pro', Roboto, Arial
  display: block
  font-weight: 300
  font-size: 100px
  color: #35495e
  letter-spacing: 1px

.subtitle
  font-weight: 300
  font-size: 42px
  color: #526488
  word-spacing: 5px
  padding-bottom: 15px

.links
  padding-top: 15px

.modal__wrapper
  position: absolute
  top: 5%
  left: 5%

.drag
  display: block
  position: absolute
  top: 20%
  right: 20%
  height: 150px
  width: 150px
  border-radius: 8%
  background: #25595C
  color: white
  cursor: grab
  &:active
    cursor: grabbing

</style>
