<template lang="">
    <div class="mainWrapper">
        <Catalog/>
        <Cart/>
    </div>
</template>
<script lang='ts'>
import Catalog from '@/components/Сatalog.vue';
import Cart from '@/components/Cart.vue';
import {defineComponent} from 'vue';
export default defineComponent ({
    name: 'mainWrapper',
    components: {
        Catalog,
        Cart
    }
})
</script>
<style lang="scss">
    .mainWrapper{
        max-width: 900px;
        margin: 0 auto;
    }
</style>