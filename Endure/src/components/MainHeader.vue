<template>
  <div class="main-header">
    <div class="main-header__brand">
      <h1 class="main-header__brand--title">Purchasing Asistant</h1>
      <h2 class="main-header__brand--subtitle">Amsterdam, the netherlands</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainHeader'
}
</script>

<style scoped>
.main-header{
  display: flex;
  flex-direction: row;
  min-height: 300px;
  background-color: #9a9a9a;
  color: white;
}
.main-header__brand{
  color: white;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 20px 0px;
  background: rgba(73, 73, 73, 0.5);
  width: 700px;
}
.main-header__brand--title{
  color: white;
  margin-top: auto;
  margin-bottom: auto;
  text-transform: uppercase;
}
.main-header__brand--subtitle{
  font-size: 20px;
  text-transform: uppercase;
}
</style>
