<template>
  <div id="app" class="admin">
    <admin/>
    <witget/>
  </div>
</template>

<script>
import admin from './components/admin'
import witget from './components/witget'

export default {
  name: 'App',
  components: {
    admin,
    witget
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans:300,300i,400,400i,600,600i,700,700i,800,800i');
*,ul,li,a{
    padding: 0;
    margin: 0;
}
li{
    list-style: none;
}
a{
    text-decoration: none;
}
body{
    font-family: 'Open Sans', sans-serif;
    background: #ecf0f1;
}
.admin{
    display: flex;
    justify-content: center;
}
</style>
