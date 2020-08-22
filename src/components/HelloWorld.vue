<template>
  <div class="hello">
  <h1>帳號<input type="text" placeholder="your email"/></h1>
  <h1>密碼<input type="text" placeholder="your password"/></h1>
  <p class="invis">{{ user }}</p>
  </div>
</template>

<script>

import { db } from '../db'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      user: [],
    }
  },

  firestore: {
    user: db.collection('user'),
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

p.invis {
  color: transparent;
}
</style>
