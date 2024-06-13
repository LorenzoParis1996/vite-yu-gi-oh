<script>
import MainCards from './MainCards.vue';
import MainSelect from './MainSelect.vue';
import axios from 'axios';


export default {
  data() {
     return {
        cards:[],
        archetypes:[]
     }
  },
  components: {
    MainCards,
    MainSelect
  },
  methods: {
    getData() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=100&offset=0')
        .then((response) => {
            this.cards = response.data.data;
            console.log(this.cards);
        });
    },
    getArchetypes() {
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
      .then((response) => {
        this.archetypes = response.data;
        console.log(response.data);
      });
    }
  },
  created() {
    this.getData();
    this.getArchetypes();
  }
}
</script>

<template>
<div class="bg">
  <MainSelect/>
  <MainCards :cards="cards"/>
</div>
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';

.bg {
  padding: 5rem;
  background-color: #d48f38;
}

</style>
