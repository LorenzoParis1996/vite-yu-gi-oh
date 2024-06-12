<script>
import MainCards from './MainCards.vue';

import axios from 'axios';


export default {
  data() {
     return {
        cards:[]
     }
  },
  components: {
    MainCards
  },
  methods: {
    getData() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
            this.cards = response.data.data;
            console.log(this.cards);
        });
    }
  },
  created() {
    this.getData();
  }
}
</script>

<template>
<div class="bg">
  <MainCards :cards="cards"/>
</div>
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';

.bg {
  padding: 2rem;
  background-color: #d48f38;
  height: 100vh;
}

</style>
