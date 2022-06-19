<template>
  <div class="api-connector">
    <ListItem :id="50" name="Sanokj" title="the end" description="shtuw" />
    <!-- make a component that accepts a list from backend and shows id, title, description, name-->
    <!-- probably have a pagination and lazy loading toggle btn -->
    <!--  -->
    <!-- connect the API -->
    <!-- return the data -->
    <!-- make a loop with the return data and loop it -->
    <i>"{{ data }}"</i>
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
    const data = ref([]);

    const loadData = async () => {
        const res = await axios.get(
            "http://localhost:3001/users/page=1&limit=500"
        );
        // page=2&limit=10&nameSort=%20&descriptSort=Net&order=desc
        data.value = res;
    };

    loadData();
    console.log(data);
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
