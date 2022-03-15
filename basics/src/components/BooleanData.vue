<template>
	<article>
        <button @click="signedIn = !signedIn" v-if="signedIn">Log In</button>
        <button @click="signedIn = !signedIn"  v-else >Log Out</button>
        <button @click="onClick" :class="{ red : deleteClicked }">Click to change color</button>
        
    </article>
</template>

<script>
export default {
  data() {
    return {
      signedIn: false,
      deleteClicked: false
    }
  },
  methods: {
    onClick() {
      this.deleteClicked = true;
    }
  }
}
</script>

<style scoped>
button {
 background-color: rgb(19, 39, 68);
 font-size: 1rem;
 font-weight: 600;
 color: white;
 padding: 1rem;
 border-radius: 5px;
}
.red {
  background-color: red;
}
</style>