<script>
export default {
    data() {
        return {
            
        }
    },
    props:{
        singleCard:{
            type: Object,
            required: true,
        }
    }

}
</script>

<template>
    
        <article>
           <img :src="singleCard.card_images[0].image_url" :alt="singleCard.name">
           <p class="white">{{ singleCard.name }}</p>
           <p>{{ singleCard.archetype }}</p>
        </article>
    
</template>



<style lang="scss" scoped>

article {
    width: calc(100% / 6);
    background-color: #d48f38;
    margin: 0.5rem;

    img {
        width: 100%;
        
    }

    p {
        text-align: center;
        font-size: 20px;
        padding: 2rem 0.5rem;

        }
    .white {
         color: white;
         font-size: 25px;
         font-weight: bold;
     }
}


</style>