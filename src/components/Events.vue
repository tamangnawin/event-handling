<template>
    <div class="cart">
        <button v-on:click="counter += 1">Add</button>
        <p>The button above has been clicked {{ counter }} times.</p>
    </div>
</template>
<script>
export default {
   data() {
    return {
        counter:0
    }
  }
}
</script>
<style scoped>
    
</style>