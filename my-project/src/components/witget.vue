<template>
   <div id="witget" class="admin--view">
      <a id="witgetimg" @click="newhospot">
          <img class="admin--view--img" src="https://respuestas.tips/wp-content/uploads/2015/04/sistema-solar-planetas.jpg" alt="">
      </a>
  </div>
</template>

<script>
export default {
  name: 'witget',
  data () {
    return {
      msg: 'no lo se rick'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.admin--view{
        width: 60%;
        margin: 10px;
        padding: 20px;
        background: #ffffff;
    }
        .admin--view--img{
            width: 100%;
        }
</style>
