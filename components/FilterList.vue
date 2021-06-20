<template>
    <div :class="$style.filter">
        <p :class="$style.title">Сортировать по: <span>цене</span></p>
        <ul :class="$style.list">
            <li :class="$style.item">По цене</li>
            <li :class="$style.item">По популярности</li>
        </ul>
    </div>
</template>

<style lang="scss" module>
.filter {
  position: relative;
  padding-top: 9px;
}

.title {
  margin: 0 0 8px 0;

  font-size: 16px;
  line-height: 21px;
  cursor: pointer;
}

.title span {
  position: relative;
  padding-right: 9px;
  color: $grey;
}

.title span::after {
  position: absolute;
  content: url('~assets/img/list-arrow.svg');
  top: -2px;
  right: 0;
  width: 5px;
  height: 2.5px;

}

.list {
  position: absolute;
  z-index: 1;
  width: 100%;
  margin: 0;
  padding: 8px 0;
  list-style: none;

  font-size: 14px;
  line-height: 18px;
  color: $grey-light;

  background: $white;
  box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.05);
  border-radius: 8px;

}

.item {
  padding: 4px 12px 4px 12px;
  cursor: pointer;
}

.item:hover,
.item:focus {
  color: $black;
  background-color: $grey-extra-light;
}
</style>