<template>
  <div :class="$style.container">
    <div :class="$style.header">
      <h1 :class="$style.title">Каталог</h1>
      <FilterList />
    </div>

    <div :class="$style.content">
      <Sidebar />
      <div :class="$style.catalog">
        <Card 
        v-for="item in items"
        :key="item.id"
        :item="item"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      items: []
    };
  },

  methods: {},

  mounted() {
    this.$axios
      .get("https://frontend-test.idaproject.com/api/product")
      .then((result) => {
        this.items = result.data;
      });
  },
};
</script>

<style lang="scss" module>
.container {
  @include container();
  padding-top: 32px;
}

.header,
.content {
  display: flex;
  justify-content: space-between;
}

.title {
  margin: 0 0 23px 0;

  font-size: 32px;
  line-height: 41px;
}

.catalog {
  width: 1104px;
  display: flex;
  flex-wrap: wrap;
}
</style>

