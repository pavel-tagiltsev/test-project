<template>
    <aside :class="$style.aside">
      <ul :class="$style.list">
        <li :class="$style.item">
          <span :class="$style.link">Рюкзаки</span>
          </li>
        <li :class="$style.item">
          <span :class="$style.link">Футболки</span>
          </li>
        <li :class="$style.item">
          <span :class="$style.link">Рубашки</span>
          </li>
      </ul>
    </aside>
</template>

<style lang="scss" module>
.list {
  margin: 0;
  padding: 0;
  list-style: none;

  font-size: 16px;
  line-height: 21px;
}

.item {
  margin-bottom: 16px;
}

.link {
  border-bottom: 1px solid $black;
  cursor: pointer; 
}

.link:hover,
.link:focus  {
  border-bottom: none;
  color: $grey;
}

.link:active {
  border-bottom: none;
  color: $grey-light;
}
</style>