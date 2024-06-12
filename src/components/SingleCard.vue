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
    
        <div>
            <img :src="singleCard.card_images[0].image_url" :alt="singleCard.name">
        </div>
        <p>
            {{ singleCard.name }}
        </p>
        <p>
            {{ singleCard.archetype }}
        </p>
    
</template>



<style lang="scss" scoped>

</style>