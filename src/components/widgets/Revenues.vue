<!-- src/components/widgets/Revenue.vue -->
<template>
  <div class="revenues-card">
    <div class="header">Revenues</div>
    <div class="percentage">
      <span class="value">15%</span>
      <span class="arrow">↗</span>
    </div>
    <p class="description">Increase compared to last week</p>
    <div class="link">
      <a href="#">Revenues report →</a>
    </div>
  </div>
</template>

<script setup>
// No script needed for static content
</script>

<style scoped>
.revenues-card {
  width: 100%;
  max-width: 300px;
  background-color: #fff;
  border-radius: 15px;
  padding: 24px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  font-family: 'Inter', sans-serif;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 200px;
  transition: box-shadow 0.3s ease;
}

.revenues-card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.08);
}

.header {
  font-size: 1.2rem;
  font-weight: 600;
  color: #111;
  margin-bottom: 10px;
}

.percentage {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  margin-bottom: 6px;
}

.value {
  font-size: 2rem;
  font-weight: 600;
  color: #111;
}

.arrow {
  color: #22c55e;
  font-size: 1.4rem;
  margin-left: 6px;
}

.description {
  font-size: 0.85rem;
  color: #555;
  margin: 8px 0;
}

.link {
  margin-top: auto;
}

.link a {
  font-size: 0.9rem;
  color: #8a5c00;
  font-weight: 500;
  text-decoration: none;
}

.link a:hover {
  text-decoration: underline;
}

/* Responsive styles */
@media (max-width: 768px) {
  .revenues-card {
    padding: 16px;
    border-radius: 12px;
  }

  .header {
    font-size: 1rem;
  }

  .value {
    font-size: 1.5rem;
  }

  .arrow {
    font-size: 1.2rem;
  }

  .description {
    font-size: 0.8rem;
  }

  .link a {
    font-size: 0.85rem;
  }
}
</style>
