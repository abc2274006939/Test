<template>
  <div id="app">
    <keep-alive  exclude="Detail">
        <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
 body{
   height:790px
 }
  body{
    margin: 0
  }
    body{
    padding: 0
  }
</style>
