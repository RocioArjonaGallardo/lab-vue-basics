<template>
<div class="add">
    <h2 class="sub">Add two numbers</h2>
    <input type="number" v-model.number="first" />
    +
    <input type="number" v-model.number="second" />
    =
    <span>{{ sum }}</span>
</div>
  
</template>

<script>
export default {
    name: 'Display',
    data: {
      first: 1,
      second: 1,
  },
    computed: {
        content: {
            sum() {
            return (this.first) + (this.second) 
            }
        }   
},
}
</script>

<style scoped>
.add {
    margin: 5rem;
}
</style>