<template>
  <nav class="nav">
    <ul class="nav-list">
      <li>Home</li>
      <li>About</li>
      <li>Contact</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
}
</script>

<style scoped>
.nav {
  background-color: brown;
  padding: 16px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav-list {
  display: flex;
  justify-content: center;
  gap: 32px;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.nav-list li {
  color: white;
  font-size: 18px;
  font-weight: 500;
  cursor: pointer;
  transition: color 0.3s ease;
}

.nav-list li:hover {
  color: #b2dfdb; 
}
</style>
