<script>
import SingleCard from './SingleCard.vue';

export default {
  data() {
     return {
       
     }
  },
  components: {
     SingleCard
  },
  props: {
    cards: {
        type: Object,
        required: true
    }
  }
}
</script>

<template>
 <div class="wrapper">
   <SingleCard v-for="(item, index) in cards" :key="item.id" :singleCard="item"/>
</div>
</template>

<style lang="scss" scoped>

</style>