<template>
  <div class="hello">
  
  </div>
</template>

<script>

const googleTrends = require('google-trends-api');

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted() {
    googleTrends.autoComplete({keyword: 'Back to School'})
    .then(function(results) {
      console.log(results);
    })
    .catch(function(err) {
      console.error(err);
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
