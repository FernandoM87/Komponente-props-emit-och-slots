<template>
    <div class="base-layout">
      <header>
        <slot name="header"></slot>
      </header>
      <main>
        <slot name="main"></slot>
      </main>
      <footer>
        <slot name="footer"></slot>
      </footer>
    </div>
  </template>
  
  <style scoped>
  .base-layout {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    min-height: 100vh;
    padding: 20px;
  }
  
  header, footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
    width: 100%;
  }
  </style>
  