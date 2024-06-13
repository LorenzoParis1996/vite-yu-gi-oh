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
  <div class="counter">

    <h2>Found {{ this.cards.length }} cards</h2>
  </div>
  <div class="wrapper">
   <SingleCard v-for="(item, index) in cards" :key="item.id" :singleCard="item"/>
</div>
</template>

<style lang="scss" scoped>

.wrapper {
    padding: 0rem 1rem 1rem;
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

}

.counter {
  background-color: #212529;
  color: white;
  padding: 1rem;
  
}

</style>