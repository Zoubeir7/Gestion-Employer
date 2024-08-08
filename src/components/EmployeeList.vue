<template>
  <div>
    <h2>Liste des employés</h2>
    <ol>
      <li v-for="employee in employees" :key="employee.id" @mouseover="hover = employee.id" @mouseleave="hover = null" :class="{ hover: hover === employee.id }">
        {{ employee.name }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: null,
      employees: [
        { id: 1, name: 'Aichetou' },
        { id: 2, name: 'sidi' },
        { id: 3, name: 'Ousmane' }
      ]
    };
  }
};
</script>

<style scoped>
ol {
  padding: 0;
  list-style: none;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #f0f0f0;
  cursor: pointer;
}

.hover {
  background-color: rgb(31, 141, 31);
}
h2{
  color : green;
}
</style>