<template>
  <div class="big-header">
    <h1>{{ message }}</h1>
    <br />
    <router-link class="button" to="/page">Play Now</router-link>
    <br />
    <button class="button" @click="handleClick">Click me up</button>
  </div>
</template>

<script>
import countService from '../services/countService';

export default {
  data() {
    return {
      message: 'Hell\'Scape'
    };
  },
  methods: {
    handleClick() {
      countService.increment();
    }
  }
};
</script>
