<template>
  <div :class="$style.modal">
    <h3 :class="$style.subtitle">Оформить заказ</h3>
    <form action="post">
      <input type="text">
      <input type="text">
      <input type="text">
    </form>
  </div>
</template>

<style lang="scss" module>
.subtitle {
  margin: 0 0 16px 0;
  padding-right: 35px;

  font-size: 18px;
  line-height: 23px;
  font-weight: 400;
  color: $grey;
}

input {
  width: 100%;
  margin-bottom: 16px;

  background: $grey-extra-light;
  border: none;
  border-radius: 8px;
}
</style>