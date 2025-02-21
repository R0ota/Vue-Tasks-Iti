<script>
export default {
  name: "Card",
  props: {
    variant: {
      type: String,
      default: "default",
    },
    title: {
      type: String,
      default: "HII",
    },
  },
};
</script>

<template>
  <div :class="variant + ' card'">
    <h3>{{ title }}</h3>
    <p class="card-content">
      <slot></slot>
    </p>
    <button v-if="title ==='Hi'" class="card-button">Click Me</button>
  </div>
</template>

<style scoped>
.card {
  background: rgba(255, 255, 255, 0.2);
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  text-align: center;
  transition: transform 0.3s ease-in-out;
  border: 1px solid rgba(255, 255, 255, 0.3);
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.card-title {
  font-size: 22px;
  font-weight: bold;
  margin-bottom: 10px;
  color: #333;
}

.card-content {
  font-size: 16px;
  color: #555;
  margin-bottom: 15px;
}

.card-button {
  background: linear-gradient(135deg, #6e8efb, #a777e3);
  color: white;
  padding: 10px 20px;
  border-radius: 8px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  transition: background 0.3s ease-in-out;
}

.card-button:hover {
  background: linear-gradient(135deg, #5a7cfb, #945be3);
}

.variant {
  border: 2px solid #6e8efb;
  background: none;
  color: #6e8efb;
}
</style>
