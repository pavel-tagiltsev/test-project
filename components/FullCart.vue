<template>
  <div>
    <p :class="$style.text">Товары в корзине</p>
    <button :class="$style.button" type="button">Перейти к выбору</button>
  </div>
</template>

<style lang="scss" module>
.text {
  margin: 0 0 25px 0;
  padding-right: 35px;

  font-size: 22px;
  line-height: 28px;
}

.button {
  padding: 14px 0 15px 0;
  width: 100%;

  font-size: 16px;
  line-height: 21px;
  color: $white;

  background: $black;
  border: none;
  border-radius: 8px;

  cursor: pointer;
}
</style>