<template>
  <div class="list-item">
    <p>{{ id }}</p>
    <p>{{ name }}</p>
    <p>{{ title }}</p>
    <p>{{ description }}</p>
  </div>
  <!-- make a component that accepts a list from backend and shows id, title, description, name-->
</template>

<script>
export default {
  name: "ListItem",
  props: {
    id: Number,
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
  width: 160px;
  height: 80px;
}
</style>
