<template>
    <div id="app">
      <BaseLayout>
        <template #header>
          <h1>Welcome to My Card App</h1>
        </template>
        
        <template #footer>
          <p>&copy; 2024 My Card App</p>
        </template>
  
        <template #main>
          <div v-for="(card, index) in cards" :key="index">
            <Card :card="card" @card-clicked="handleCardClick">
              Contact {{ card.title }}
            </Card>
          </div>
        </template>
      </BaseLayout>
    </div>
  </template>
  
  <script>
  import Card from "@/components/Card.vue";
  import BaseLayout from "@/components/BaseLayout.vue";
  
  export default {
    components: {
      Card,
      BaseLayout,
    },
    data() {
      return {
        cards: [
          { title: "Dracula", description: "The famous vampire" },
          { title: "The Shining", description: "A classic horror movie" },
          // Add more cards as needed
        ],
      };
    },
    methods: {
      handleCardClick(clickedCard) {
        console.log(`Clicked on ${clickedCard.title}`);
      },
    },
  };
  </script>
  
  <style>
  #app {
    min-height: 100vh;
  }
  
  </style>
