<script>
export default {
    // option 1 reactive data
  data() {
    return {
      count: 0,
    };
  },
    // option2 functions
  methods: {
    increase() {
      this.count++;
    },
    decrease() {
      if (this.count > 0) {
        this.count--;
      }
    }
  }
};
</script>

<template>
  <main>
    <h1>Vue Counter Application</h1>

    <p :class="count > 5 ? 'red-text' : 'blue-text'">Counter: {{ count }}</p>
    <div class="buttons">
      <button @click="increase" class="btn increase">Increase</button>
      <button @click="decrease" class="btn decrease">Decrease</button>
    </div>
  </main>
</template>

<style scoped>
body {
  background: linear-gradient(to right, #6a11cb, #2575fc);
  font-family: 'Poppins', sans-serif;
}
main {
  display: flex;
  flex-direction: column;
  gap: 20px;
  align-items: center;
  justify-content: center;
  height: 100vh;
  text-align: center;
}
h1 {
  font-size: 2.5rem;
  color: black;
  text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
}
p {
  font-size: 2rem;
  font-weight: bold;
  padding: 10px 20px;
  border-radius: 8px;
  background: white;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}
.red-text {
  color: red;
}

.blue-text {
  color: blue;
}

.buttons {
  display: flex;
  gap: 15px;
}

.btn {
  padding: 12px 20px;
  font-size: 1.2rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: bold;
}


.increase {
  background-color: #28a745;
  color: white;
}

.increase:hover {
  background-color: #218838;
  transform: scale(1.1);
}


.decrease {
  background-color: #dc3545;
  color: white;
}

.decrease:hover {
  background-color: #c82333;
  transform: scale(1.1);
}
</style>
