<template>
    <div class="card">
      <h2>{{ card.title }}</h2>
      <p>{{ card.description }}</p>
      <button @click="emitCardClick">
        <slot>Contact {{ card.title }}</slot>
      </button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      card: Object,
    },
    methods: {
      emitCardClick() {
        this.$emit('card-clicked', this.card);
      },
    },
  };
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    padding: 20px;
    margin: 10px;
    border-radius: 5px;
  }
  
  button {
    background-color: #4caf50;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 3px;
    cursor: pointer;
  }
  </style>
  