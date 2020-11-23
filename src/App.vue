<template>
  <div class="min-h-screen" id="app">
    <h1 class="text-center text-2xl p-4 font-bold text-gray-800 bg-white">
      My Birthday Wishlist
    </h1>
    <!-- component -->
    <div class="container w-full sm:w-1/2 mx-auto row mt-4">
      <div v-for="(wish, index) in list" :key="index"  class="col-md flex flex-col justify-center px-20 py-10 my-2 mx-2 bg-white rounded-lg shadow-2xl">
        <div class="prod-title">
          <p class=" text-gray-900 font-bold text-center">
            {{ wish.name }}
          </p>
        </div>
        <div class="prod-img mt-2">
          <img :src="wish.img" class="w-full object-cover object-center" />
        </div>
        <div class="prod-info grid gap-10 mt-3">
          <div class="flex flex-col md:flex-row justify-between items-center text-gray-900">
            <p class="font-bold text-xl">₦ {{ wish.price }}</p>
            <a :href="wish.url" class="px-6 py-2 transition ease-in duration-200 uppercase rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none">
              View
            </a>
          </div>
        </div>
      </div>
    </div>

    <p class="footer bg-white text-center p-3 mt-4">
      With Love, oluwakayode
    </p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        list: [
          {
            name: 'Yamaha PSR E463',
            img: 'https://ng.jumia.is/unsafe/fit-in/680x680/filters:fill(white)/product/02/554334/1.jpg?8656',
            price: '150,000',
            url: ''
          },
          {
            name: 'Havit M29 Bluetooth Speaker',
            img: 'https://ng.jumia.is/unsafe/fit-in/680x680/filters:fill(white)/product/85/031326/1.jpg?3937',
            price: '10,000',
            url: 'https://www.jumia.com.ng/havit-m29-bluetooth-wireless-speaker-with-alarm-clock-62313058.html'
          },
          {
            name: 'Tshirtssss',
            img: 'https://www.redwolf.in/image/catalog/mens-t-shirts/david-bowie-heroes-tshirt-india.jpg',
            price: 'Varies',
            url: ''
          },
          {
            name: 'Whiteboard',
            img: 'https://ng.jumia.is/unsafe/fit-in/680x680/filters:fill(white)/product/05/936326/1.jpg?1259',
            price: '9,000',
            url: 'https://www.jumia.com.ng/generic-whiteboard-for-all-classrooms-3ft-x-4ft-61202619.html'
          },
          {
            name: 'We All Should Be Feminists',
            img: 'https://images-na.ssl-images-amazon.com/images/I/41iXPOubV8L._AC_SY400_.jpg',
            price: '1,500',
            url: 'https://www.jumia.com.ng/jumia-books-we-should-all-be-feminists-7097807.html'
          },
          {
            name: 'This is Our God: His Wrath',
            img: 'https://images-na.ssl-images-amazon.com/images/I/41IyAvjRSEL._SX331_BO1,204,203,200_.jpg',
            price: '10,000',
            url: ''
          },
          {
            name: 'Cash',
            img: require('./assets/img.png'),
            price: '∞',
            url: ''
          },
          {
            name: 'Samsung Galaxy A10s',
            img: 'https://ng.jumia.is/unsafe/fit-in/680x680/filters:fill(white)/product/16/433524/4.jpg?8205',
            price: '46,990',
            url: 'https://www.jumia.com.ng/samsung-galaxy-a10s-6.2-inch-2gb32gb-rom-android-9.0-13mp2mp-8mp-dual-sim-4000mah-4g-lte-smartphone-black-42533461.html'
          },
          {
            name: 'Sneakers (Size 45)',
            img: require('./assets/shoe.svg'),
            price: 'Varies',
            url: ''
         },
         {
           name: 'Complete Web & Mobile Designer in 2020',
           img: 'https://img-b.udemycdn.com/course/240x135/3227583_5e75_5.jpg?secure=2GWWCpl7t2pO8kAzeSJVJg%3D%3D%2C1606198949',
           price: '7,000',
           url: 'https://www.udemy.com/course/complete-web-designer-mobile-designer-zero-to-mastery/'
         },
         {
           name: 'The Complete Guide to Django REST Framework and Vue JS',
           img: 'https://img-b.udemycdn.com/course/240x135/2257152_acc5_7.jpg?secure=V5OjvCbZ8bw6EYPh6NwEYg%3D%3D%2C1606199029',
           price: '7,000',
           url: 'https://www.udemy.com/course/the-complete-guide-to-django-rest-framework-and-vue-js/'
         },
         {
           name: 'UI UX Web Design Using Adobe XD',
           img: 'https://img-a.udemycdn.com/course/240x135/1452908_8741_3.jpg?e5foF_rWu4hkq_QMh5I8qIqH6VdraFVIDCqKUPzl-0PFc7DK0moAno_u1il0At05HaxX6j3n3WWREpCBk9aQhgNeyL_Rj_V5Tawa6w3rQbvphNCTJmahTRuWTn9jtoCP',
           price: '7,000',
           url: 'https://www.udemy.com/course/ui-ux-web-design-using-adobe-xd/'
         },
        ]
      }
    }
}
</script>

<style scoped>
  @import url('./assets/bootstrap-grid.min.css');
  #app {
    background: url('./assets/cool-background.png') no-repeat;
    background-size: cover;
  }
</style>
