<template>
  <div id="app">
    <Header class="header" />
    <NotFound />
    <Footer class="footer" />
  </div>
</template>

<script>
export default {}
</script>

<style>
body {
  margin: 0px;
  background-color: black;
}
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  max-width: 600px;
  width: 100%;
  margin: auto;
}
.header {
  margin-bottom: 16px;
}
.footer {
  margin-top: auto;
}
</style>
