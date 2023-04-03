<template>
  <div class="home">
    <h1>Home</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click Me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name" />

    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Update Ninja One</button>

    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
    <button @click="updateNinjaTwo">Update Ninja Two</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";

export default {
  name: "Home",
  setup() {
    // const p = ref(null)

    const name = ref("Emmanuel");
    const age = ref(24);

    const handleClick = () => {
      // console.log(p, p.value)
      // p.value.classList.add('test')
      // p.value.textContent = 'Hello User'

      name.value = "Samuel";
      age.value = 19;
    };

    // for Refs and Reactive section
    const ninjaOne = ref({ name: "Gloria", age: 16 });
    const ninjaTwo = reactive({ name: "Mercy", age: 15 });

    const updateNinjaOne = () => {
      ninjaOne.value.age = 21;
    };

    const updateNinjaTwo = () => {
      ninjaTwo.age = 20;
    };

    return {
      name,
      age,
      handleClick,
      ninjaOne,
      ninjaTwo,
      updateNinjaOne,
      updateNinjaTwo,
    };
  },
};
</script>
