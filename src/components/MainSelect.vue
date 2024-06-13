<script>
export default {
    data() {
        return {
           
        }
    },
    props: {
        archetypes: {
            type: Object,
            required: true
        }
    }
}

</script>


<template>
<select name="" id="">
 <option value="none">Filter</option>
 <option v-for="(item, index) in archetypes" :key="index"  value="index" @click="$emit('searched', index)">{{ item.archetype_name }}</option>

</select>

</template>


<style lang="scss" scoped>
select {
    margin-bottom: 2rem;
    padding: 0.5rem 3rem 0.5rem 0.5rem;
    font-size: 20px;
}

</style>