<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />

    <!-- <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click Me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name" />

    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Update Ninja One</button>

    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
    <button @click="updateNinjaTwo">Update Ninja Two</button>

    <h2>Computed Properties</h2>
    <input type="text" v-model="search" />
    <p>search term - {{ search }}</p> -->
    <!-- <div v-for="name in names" :key="name">{{ name }}</div> -->
    <!-- <div v-for="name in matchingNames" :key="name">{{ name }}</div> -->
  </div>
</template>

<script>
import { ref, reactive, computed, watch } from "vue";
import PostList from "../components/PostList.vue";

export default {
  name: "Home",
  components: { PostList },
  setup() {
    // const p = ref(null)

    // const name = ref("Emmanuel");
    // const age = ref(24);

    // const handleClick = () => {
    // console.log(p, p.value)
    // p.value.classList.add('test')
    // p.value.textContent = 'Hello User'

    //   name.value = "Samuel";
    //   age.value = 19;
    // };

    // for Refs and Reactive section
    // const ninjaOne = ref({ name: "Gloria", age: 16 });
    // const ninjaTwo = reactive({ name: "Mercy", age: 15 });

    // const updateNinjaOne = () => {
    //   ninjaOne.value.age = 21;
    // };

    // const updateNinjaTwo = () => {
    //   ninjaTwo.age = 20;
    // };

    // for computed properties
    // const search = ref('')
    // const names = ref(['peace', 'joel','favour', 'gloria','samuel','mercy','blessed'])

    // watch(search, () =>{
    //   console.log('watch function ran')
    // })

    // const matchingNames = computed(() => {
    //   return names.value.filter((name) => name.includes(search.value))
    // })

    // for props
    const posts = ref([
      { title: "welcome to the blog", body: "Lorem ipsum", id: 1 },
      { title: "top 5 CSS tips", body: "Lorem ipsum", id: 2 },
    ]);

    return {
      // name,
      // age,
      // handleClick,
      // ninjaOne,
      // ninjaTwo,
      // updateNinjaOne,
      // updateNinjaTwo,
      // names,
      // search,
      // matchingNames

      posts,
    };
  },
};
</script>
