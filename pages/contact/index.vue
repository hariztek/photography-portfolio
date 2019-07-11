<template>
  <div class="bg">
    <div id="app">
      <Form />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .bg {
    background-image: url("../../assets/contact_bg.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding-bottom: 21%;
    color: white;
    overflow: hidden;
  }

</style>

<script>
  import Form from "~/components/Form/Form"
  export default {
    head() {
      return {
        title: 'Contact Me',
        meta: [{
          hid: 'description',
          meta: 'description',
          content: 'put your content here'
        }]
      }
    },
    components: {
      Form
    }
  }

</script>
