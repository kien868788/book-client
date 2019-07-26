<template>
  <div class="home page">
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  components: {
  },

  data () {
    return {
      msg: 'Welcome to Index!!!',
      isShownModal: false,
      inputError: false,
      checkboxState: false,

      pagination: {
        limit: 20,
        offset: 0,
        total: 60
      }
    }
  },

  methods: {
    showToast () {
      console.log('aaa')
      this.$store.commit('toast/NEW', { type: 'success', message: 'hello' })
    },
    submitModalHandler () {
      // some logic
      this.isShownModal = false
    },
    onBlur () {
      console.log('onBlur!!!')
    },
    onEnter () {
      console.log('onEnter!!!')
    },
    onEsc () {
      console.log('onEsc!!!')
    },
    onClickIcon () {
      console.log('onClickIcon!!!!')
    }
  }
}
</script>

<style lang="scss" scoped>
.some-modal-content {
  min-width: 400px;
  padding: 25px;

  .buttons button {
    padding: 10px;
    margin: 10px;
  }
}
</style>
