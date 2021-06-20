<template>
  <div :class="$style.modal">
    <section :class="$style.content">
      <h2 :class="$style.title">Корзина</h2>
      <h3 :class="$style.subtitle">Товары в корзине</h3>
      <ul :class="$style.list">
        <BascetCart />
        <BascetCart />
        <BascetCart />
      </ul>
      <Form/>
      <button :class="$style.button" type="button">Перейти к выбору</button>
      <button :class="$style.cross" type="button" aria-label="Закрыть корзину">
        <svg
          width="14"
          height="14"
          viewBox="0 0 14 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M13.7071 0.292893C14.0976 0.683417 14.0976 1.31658 13.7071 1.70711L1.70711 13.7071C1.31658 14.0976 0.683417 14.0976 0.292893 13.7071C-0.0976311 13.3166 -0.0976311 12.6834 0.292893 12.2929L12.2929 0.292893C12.6834 -0.0976311 13.3166 -0.0976311 13.7071 0.292893Z"
            fill="black"
          />
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M0.292893 0.292893C0.683417 -0.0976311 1.31658 -0.0976311 1.70711 0.292893L13.7071 12.2929C14.0976 12.6834 14.0976 13.3166 13.7071 13.7071C13.3166 14.0976 12.6834 14.0976 12.2929 13.7071L0.292893 1.70711C-0.0976311 1.31658 -0.0976311 0.683417 0.292893 0.292893Z"
            fill="black"
          />
        </svg>
      </button>
    </section>
  </div>
</template>

<style lang="scss" module>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;

  width: 100%;
  height: 100%;

  background-color: fade-out($white, 0.2);
}

.content {
  position: relative;

  margin-left: auto;
  padding: 52px 48px;
  width: 460px;
  height: 100%;
  background-color: $white;

  color: $black-true;

  box-shadow: -4px 0px 16px rgba(0, 0, 0, 0.05);
  border-radius: 8px 0px 0px 8px;
}

.title {
  margin: 0 0 25px 0;

  font-size: 32px;
  line-height: 41px;
}

.subtitle {
  margin: 0 0 16px 0;
  padding-right: 35px;

  font-size: 18px;
  line-height: 23px;
  font-weight: 400;
  color: $grey;
}

.list {
  margin: 0;
  padding: 0;
  list-style: none;
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

.cross {
  position: absolute;
  top: 50px;
  right: 34px;
  width: 50px;
  height: 50px;

  border: none;
  background-color: transparent;
  cursor: pointer;
}
</style>