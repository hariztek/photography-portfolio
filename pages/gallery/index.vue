Image 1 Image 2 Image 3 Image 4 Image 5 Image 6 Image 7 Image 8
<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-lg-4 col-md-4 col-sm-12 col-xs-1">
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(80)" alt="Image 1"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(82)" alt="Image 2"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(84)" alt="Image 3"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(85)" alt="Image 4"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(88)" alt="Image 5"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(90)" alt="Image 6"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(92)" alt="Image 7"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(94)" alt="Image 8"></b-img-lazy>
        </div>
        <div class="col-lg-4 col-md-4 col-sm-12 col-xs-1">
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(1)" alt="Image 1"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(2)" alt="Image 2"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(3)" alt="Image 3"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(4)" alt="Image 4"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(45)" alt="Image 5"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(34)" alt="Image 6"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(54)" alt="Image 7"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(21)" alt="Image 8"></b-img-lazy>
        </div>
        <div class="col-lg-4 col-md-4 col-sm-12 col-xs-1">
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(44)" alt="Image 1"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(55)" alt="Image 2"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(66)" alt="Image 3"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(34)" alt="Image 4"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(21)" alt="Image 5"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(22)" alt="Image 6"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(26)" alt="Image 7"></b-img-lazy>
          <b-img-lazy v-bind="mainProps" :src="getImageUrl(56)" alt="Image 8"></b-img-lazy>
        </div>
      </div>
    </div>
    <no-ssr>
      <lightbox thumbnail="https://res.cloudinary.com/hariztek/image/upload/v1541144762/luxury%20inn/room3.jpg"
        :images="['https://res.cloudinary.com/hariztek/image/upload/v1541144762/luxury%20inn/room3.jpg']">
      </lightbox>
    </no-ssr>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        mainProps: {
          center: true,
          fluidGrow: true,
          blank: true,
          blankColor: '#bbb',
          width: 600,
          height: 400,
          class: 'my-5 gal'
        }
      }
    },
    methods: {
      getImageUrl(imageId) {
        const {
          width,
          height
        } = this.mainProps
        return `https://picsum.photos/${width}/${height}/?image=${imageId}`
      },
      head() {
        return {
          title: 'Gallery',
          meta: [{
            hid: 'description',
            meta: 'description',
            content: 'put your content here'
          }]
        }
      }
    }
  }

</script>

<style lang="scss" scoped>
  .gal {
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.57);
  }

</style>
