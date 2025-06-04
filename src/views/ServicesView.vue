<template>
  <div>
    <!-- <h1>{{ title }}</h1> -->
    <!-- <p>{{ description }}</p> -->
    <!-- <h1 v-if="instock">Item in stock</h1> -->
    <!-- <p v-else>Not in stock</p> -->
    <!-- <p v-if="smartphones > 3"> smartphones in stock</p> -->
    <h1 v-if="day == 'monday'">Time to work</h1>
    <h1 v-else-if="day == 'tuesday'">You survived monday</h1>
    <h1 v-else-if="day == 'wednesday'">You survived tuesday</h1>
    <h1 v-else-if="day == 'thursday'">You survived wednesday</h1>
    <h1 v-else-if="day == 'friday'">Welcome to the weekend</h1>
    <h1 v-else-if="day == 'saturday'">The weekend continues</h1>
    <h1 v-else>It's almost monday</h1>
  </div>
</template>

<script>
export default {
  name: "ServicesView",
  data() {
    return {
      // title: "Hello",
      // description: "Welcome",
      // instock: true,
      // smartphones: 4,
      day: "monday",
    };
  },
};
</script>
