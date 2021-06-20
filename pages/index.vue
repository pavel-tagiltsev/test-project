<template>
  <div :class="$style.container">
    <div :class="$style.header">
      <h1 :class="$style.title">Каталог</h1>
      <FilterList />
    </div>

    <div :class="$style.content">
      <Sidebar />
      <div :class="$style.catalog">
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
      </div>
    </div>
  </div>
</template>

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

