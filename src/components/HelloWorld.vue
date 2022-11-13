<template>
    <h1>{{ msg }}</h1>
    <BaseInput
        v-model="email"
        @blur="email = 'blurrr@its.cold'"
        label="Email:"
        type="email"
        class="thicc"
    />
    <pre>{{ email }}</pre>
</template>

<script>
import { ref } from 'vue'
import BaseInput from '@/components/BaseInput'

export default {
  name: 'App',
  props: {
    msg: String
  },
  components: {
    BaseInput
  },
  setup () {
    const email = ref('')
    return {
      email
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
</style>
