<script>
export default {
  data() {
    return {
      toggle: true,
      count: 1,
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      },

    }
  },
  computed: {
    publishedBooksMessage() {
      return this.author.books.length > 0 ? 'yes' : 'no'
    },


  },
  methods: {
    num() {
      this.count++;
      // console.log(this.count);
    },

  },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  
}
</script>

<template>
  <div class="hello">
    <h1 v-if="toggle">{{ msg }}</h1>
    <h2>{{ count }}</h2>
    <button @click="num">ADD 1</button>
    <p>Has published books:</p>
    <span>{{ publishedBooksMessage }}</span>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
