<template>
  <div class="w-screen h-screen bg-gray-500 p-20 overflow-auto"> <!-- Parent -->
    <div class="text-yellow-300 text-2xl">
      PARENT <i class="fas fa-igloo"></i>
    </div>  
      <div class="flex-auto w-full bg-blue-500 md:bg-red-500 p-14 text-yellow-400 m-20"> <!-- Child -->
        CHILD1
      </div>
      <div class="flex-auto w-1/2 bg-red-500 md:bg-blue-500 p-14 text-yellow-400 m-20"> <!-- Child -->
        CHILD2 {{ productName }}
        <testimonial
          image_src="https://images.unsplash.com/photo-1499714608240-22fc6ad53fb2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80"
          name="Alex"
          title="Welcome"
          content="Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae dolores deserunt ea doloremque natus error, rerum quas odio quaerat nam ex commodi hic, suscipit in a veritatis pariatur minus consequuntur!"
        >
        </testimonial>
      </div>
  </div>
</template>

<script>
import {mapState} from 'vuex';
export default {
  computed:{
    ...mapState({
      productName: state => state.product.productName
    })
  }

}
</script>

<style>

</style>
Testimonial