<template>
  <div class="app">
    <div class="">
      <div class="col-md-12">
        <div class="row">
          <hr>
          <div class="gal">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <h1 class="text-center title">Lorem, ipsum dolor.</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, aperiam similique aliquid velit, ut omnis
              eum labore consequatur minima necessitatibus aliquam pariatur rem officiis ipsa distinctio explicabo
              expedita molestiae recusandae consectetur hic porro repellendus! Blanditiis ducimus molestiae nostrum
              culpa, maxime, facilis animi sapiente inventore facere dolorem recusandae nihil voluptatem! Perferendis!
            </p>
            <img src="https://preview.ibb.co/mWpE3Q/2.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/3.jpg" alt="">
            <img src="https://preview.ibb.co/mysOxk/3.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/mWpE3Q/2.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
            <img src="https://preview.ibb.co/i0PmHk/1.jpg" alt="">
          </div>
          <div class="col-lg-6">
            <no-ssr>
              <lightbox thumbnail="https://res.cloudinary.com/hariztek/image/upload/v1541144761/luxury%20inn/room1.jpg"
                :images="['https://res.cloudinary.com/hariztek/image/upload/v1541144761/luxury%20inn/room1.jpg']">
              </lightbox>
            </no-ssr>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .gal {
    -webkit-column-count: 3;
    /* Chrome, Safari, Opera */
    -moz-column-count: 3;
    /* Firefox */
    column-count: 3;
  }

  .gal img {
    width: 100%;
    padding: 7px 0;
  }

  .title {
    text-transform: uppercase;
    background-color: black;
    color: white;
  }

  @media (max-width: 500px) {
    .gal {
      -webkit-column-count: 1;
      /* Chrome, Safari, Opera */
      -moz-column-count: 1;
      /* Firefox */
      column-count: 1;
    }
  }

</style>

<script>
  export default {
    head() {
      return {
        title: 'Home',
        meta: [{
          hid: 'description',
          meta: 'description',
          content: 'put your content here'
        }]
      }
    }
  }

</script>
