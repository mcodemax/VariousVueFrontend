<template>
  <div class="api-connector">
    <!-- make a component that accepts a list from backend and shows id, title, description, name-->
    <!-- probably have a pagination and lazy loading toggle btn -->
    <div v-for="item in data" :key="item.id">
        <ListItem :key="item.id" :id="item.id" :name="item.name" :title="item.title" :description="item.description"/>
    </div>
  </div>
  <!-- make a component that accepts a list from backend and shows id, title, description, name-->
</template>

<script>
import ListItem from "./ListItem.vue";
import axios from "axios";
import { ref } from "vue";

export default {
  name: "APIConnector",
  components: {
    ListItem,
  },
  setup() {
    const data = ref("");

    const loadData = async () => {
        const res = await axios.get(
            "http://localhost:3001/users?page=1&limit=50"
        ); //page=1&limit=50&nameSort=%20&descriptSort=Net&order=desc
        // have state that has a function to toggle asc/desc data sorts and change search criteria
        res.data.results.unshift({id:'ID', name:'Name', title: 'Title', description:'Description'});
        data.value = res.data.results;
    };

    loadData();
    console.log(data);

    return {
        data
    };
  },
  
};
</script>

<style>
.api-connector {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
