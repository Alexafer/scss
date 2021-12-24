<template lang="">
  <div class="catalog">
    <h1>Catalog</h1>
    <div class="catalog__list">
      <CatalogItem
        @sendArticle="showChild"
        v-for="product in products"
        :key="product.article"
        :product_data="product"
      />
    </div>
  </div>
</template>
<script lang="ts">
import CatalogItem from '@/components/CatalogItem.vue';
import {defineComponent} from 'vue';
export default defineComponent({
  name: 'Catalog',
  components: {
    CatalogItem,
  },
  props: {},
  data() {
    return {
      products: [
        {
          image: '1.jpg',
          name: 'T-shirt 1',
          price: 100,
          article: 'T1',
          available: 'true',
        },
        {
          image: '2.jpg',
          name: 'T-shirt 2',
          price: 150,
          article: 'T2',
          available: 'true',
        },
        {
          image: '3.jpg',
          name: 'T-shirt 3',
          price: 200,
          article: 'T3',
          available: 'false',
        },
      ],
    };
  },
  computed: {},
  methods: {
    showChild(data: Object) {
      console.log(data);
    },
  },
});
</script>
<style lang="scss">
.catalog {
  &__list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
  }
}
</style>
