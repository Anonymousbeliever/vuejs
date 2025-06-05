<template>
  <div>
    <!-- DATA TYPES -->
    <!-- <h1>{{ title }}</h1> -->
    <!-- <p>{{ description }}</p> -->
    <!-- <h1 v-if="instock">Item in stock</h1> -->
    <!-- <p v-else>Not in stock</p> -->
    <!-- <p v-if="smartphones > 3"> smartphones in stock</p> -->
    <!-- <h1 v-if="day == 'monday'">Time to work</h1>
    <h1 v-else-if="day == 'tuesday'">You survived monday</h1>
    <h1 v-else-if="day == 'wednesday'">You survived tuesday</h1>
    <h1 v-else-if="day == 'thursday'">You survived wednesday</h1>
    <h1 v-else-if="day == 'friday'">Welcome to the weekend</h1>
    <h1 v-else-if="day == 'saturday'">The weekend continues</h1>
    <h1 v-else>It's almost monday</h1> -->

    <!-- ARRAYS -->
    <!-- <p v-for="(fruit, index) in fruits" :key="index">{{ fruit }}</p> -->
    <h1>Blogs</h1>
    <!-- <img v-bind:src="imgurl" alt="" srcset="" /> -->
    <div class="parent">
      <div v-for="(blog, index) in blogs" :key="index" class="card">
        <h3>{{ blog.id }}</h3>
        <h4>{{ blog.title }}</h4>
        <p>{{ blog.price }}</p>
        <img v-bind:src="blog.image" alt="">
      </div>
    </div>
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
      //   day: "monday",
      //   fruits: ["oranges", "mangoes", "bananas", "apples"],
      blogs: [],
      imgurl: "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg"
    };
  },
  mounted() {
    // alert("hey");
    fetch("https://fakestoreapi.com/products")
      .then((response) => response.json())
      // .then(json => console.log(json));
      .then((data) => {
        this.blogs = data;
      });
  },
};
</script>
<style scoped>
.parent {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.card {
  background-color: tomato;
  margin: 5px;
  padding: 5px;
  width: 250px;
}
img{
  width: 200px;
  height: 200px;
}
</style>
