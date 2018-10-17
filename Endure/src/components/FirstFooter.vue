<template>
  <div class="first-footer">
   <div class="first-footer__contents">
   </div>
  </div>
</template>

<script>
export default {
  name: 'FirstFooter',
  data () {
    return {
    }
  },
  mounted () {
  }
}
</script>

<style lang="scss" scoped>
.first-footer{
  background-color: rgb(39, 39, 39);
  min-height: 400px;
  margin-top: 0px;
}
.first-footer__contents{
  display: flex;
  background-color: white;
  width: 700px;
}
</style>
