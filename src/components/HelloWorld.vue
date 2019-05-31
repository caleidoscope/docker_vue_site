<template>
   <div class="buttons">
            <b-button type="is-primary">{{message}}</b-button>

            <b-button type="is-success">Success</b-button>

            <b-button type="is-danger">Danger</b-button>
 
            <b-button type="is-warning">Warning</b-button>
        
            <b-button type="is-info">Info</b-button>
        
            <b-button type="is-link">Link</b-button>

            <b-button type="is-light">Light</b-button>

            <b-button type="is-dark" @click="changeText">Dark</b-button>

            <b-button type="is-text">{{envvar}}</b-button>
        </div>
</template>

<script>
export default {
  data: ()=>{
    return {
      message:'hello from World',
      envvar: process.env.VUE_APP_TEST}
    },
  props: {
    msg: String
  },
  methods: {
    changeText() {
      this.message = 'something else!'
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
</style>
