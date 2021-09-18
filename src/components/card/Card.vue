<template>
  <div class="card">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: "card",
};
</script>
<style lang="scss" scoped>
.card {
  width: 80%;
  margin: 25px auto;
  border-radius: 10px;
  box-shadow: 0 0 40px -10px #3c71e040;
  padding: 20px;
}
</style>
