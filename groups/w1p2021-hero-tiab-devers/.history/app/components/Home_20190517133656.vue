<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <br />
    <router-link class="button" to="/characters">Play</router-link>
    <br />
    <router-link class="button" to="/page">Continue</router-link>
    <br />
    <router-link class="button" to="/page">New game</router-link>
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
