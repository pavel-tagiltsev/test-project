<template>
  <aside :class="$style.aside">
    <ul :class="$style.list">
      <li
        :class="$style.item"
        v-for="category in categories"
        :key="category.id"
      >
        <span :class="$style.link">{{ category.name }}</span>
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  data: function () {
    return {
      categories: [],
    };
  },

  methods: {},

  mounted() {
    this.$axios
      .get("https://frontend-test.idaproject.com/api/product-category")
      .then((result) => {
        this.categories = result.data;
      });
  },
};
</script>

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
.link:focus {
  border-bottom: none;
  color: $grey;
}

.link:active {
  border-bottom: none;
  color: $grey-light;
}
</style>