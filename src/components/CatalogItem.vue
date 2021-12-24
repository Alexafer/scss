<template lang="">
<div> 
    <div class="catalogItem">
        <img class="catalogItem__image" :src="require('../assets/images/' + product_data.image)"  alt="img">
        <p class="catalog-item__name">{{product_data.name}}</p>
        <p class="catalog-item__price">Price: {{product_data.price}}</p>
        <button class="catalog-item__add_to_cart_btn btn" @click="this.$emit('sendArticle', this.product_data.article)">Add to cart</button>
    </div>
</div>
    
</template>
<script lang="ts">
import {defineComponent} from 'vue';
export default defineComponent ({
    name: 'CatalogItem',
    components: {},
    props: {
        product_data: {
            type: Object,
            default() {
                return {}
            }
        }
    },
    data(){
        return {
        }
    },
    methods: {
        // sendData(){
            
        // }
    }
})
</script>
<style lang="scss">
@import "@/scss/styles.scss";
  .catalogItem {
      border: 2px solid red;
      flex-basis: 25%;
      box-shadow: 0 0 8px 0 #e0e0e0;
      padding: $paddinuu*2;
      margin-bottom: $marginuu*2;
      &__image {
          width: 100px;
      }
  }
</style>