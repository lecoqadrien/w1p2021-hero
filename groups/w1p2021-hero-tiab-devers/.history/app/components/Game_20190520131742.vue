<template>
<div>
  <h1>{{ step.title }}</h1>

  <ul>
    <li v-for="(action, index) in step.actions" :key="index">
      <router-link :to="action.to.toString()">
        {{ }}
      </router-link>
    </li>
  </ul>
</div>
</template>

<script>
import game from '../data.json';
console.log(game);

export default {
  computed: {
    step() {
      return game.steps.find(step => {
        return step.id === parseInt(this.$route.params.id)
      })
    }
  },
  mounted: function() {
    console.log('Is Mounted');
  }
}
</script>
