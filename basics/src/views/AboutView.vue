<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Display />
    <Cards />
  </div>
</template>

<script>
// @ is an alias to /src
import Display from '@/components/Display.vue';
import Cards from "@/components/Cards.vue";

export default {
  name: 'AboutView',
  components: {
    Display,
    Cards
  }
}
</script>