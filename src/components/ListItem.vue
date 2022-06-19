<template>
  <div class="list-item">
    <p>{{ id }}</p>
    <p>{{ name }}</p>
    <p>{{ title }}</p>
    <p class="description">{{ description }}</p>
  </div>
  <!-- make a component that accepts a list from backend and shows id, title, description, name-->
</template>

<script>
export default {
  name: "ListItem",
  props: {
    id: undefined,
    name: String,
    title: String,
    description: String,
  },
};
</script>

<style>
.list-item {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
p {
  box-sizing: border-box;
  height: 80px;
  max-width: 200px;
  min-width: 200px;
  min-height: 80px;
  max-height: 80px;
  margin: 50px;
  color: rgb(124, 111, 137);
}
.description {
  box-sizing: border-box;
  height: 80px;
  max-width: 1000px;
  min-width: 1000px;
  min-height: 80px;
  max-height: 80px;
  overflow: hidden;
  margin: 50px;
  color: rgb(124, 111, 137);
}
</style>
