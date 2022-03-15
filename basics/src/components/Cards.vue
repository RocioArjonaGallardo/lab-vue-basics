<template>
  <div class="container">
      <div class="card" v-for="card in cards" :key="card.id">
          <h2>{{ card.title }}</h2>
          <p>{{ card.content }}</p>
      </div>

  </div>
</template>

<script>
export default {
    name: "cards",
    data () {
        return {
            cards: [],
        };
    },
    methods: {
        async getCards() {
            const res = await fetch("http://localhost:3000/cards");
            const finalRes = await res.json();
            this.cards = finalRes;
        }
        },
    mounted () {
        this.getCards()
    }
    }

</script>

<style scoped>
.card {
    display: grid;
    grid-column: 1fr;
    grid-template-rows: auto;
    border: 1px black solid;
    margin: 1rem;
}
h2 {
    font-size: 1.3rem;
    color:black;
}
 p{
     font-size: 1rem;
     color: black;
 }
</style>