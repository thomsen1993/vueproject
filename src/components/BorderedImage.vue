<template>
    <div class="borderedImage">
      <img :src="imageSrc" alt="Border Image" />
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageSrc: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .borderedImage {
    border: 2px solid #000; /* Adjust border thickness and color as needed */
    border-radius: 8px; /* Adjust border radius as needed */
    overflow: hidden; /* Ensure image does not extend beyond border */
  }
  
  .borderedImage img {
    display: block;
    width: 100%;
    height: auto;
  }
  </style>
  