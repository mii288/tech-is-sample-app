<template>
  <div class="container">
    <ul>
      <li v-for="animal in animals" :key="animal.name">
        <a :href="`/${animal.name}`" class="card">
          <h2>{{animal.name}}<img :src="require(`~/assets/img/${animal.image}`)" height="100"></h2>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animals: [
        {name: 'cat', image: 'cat.png'},
        {name: 'dog', image: 'dog.png'},
        {name: 'mouse', image: 'mouse.png'},
        {name: 'elephant', image: 'elephant.png'}
      ]
    }
  }
}
</script>

