<template>
  <header class="header flex row" @click="backHome">
    <div class="header__left flex row a-center j-start">
      <img src="../assets/background_invoice.svg" alt="" />
      <h1>Invoice Manager</h1>
      <svg
        class="header__left_svg"
        width="232"
        height="39"
        viewBox="0 0 232 39"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M4 35C159.893 -1.35364 218.289 1.63977 228 7.68067"
          stroke="#11EF5C"
          stroke-width="7"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </div>
    <div class="header__right flex row a-center j-end">
      <h4>Sign out</h4>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
  methods: {
    backHome() {
      this.$router.push({ name: 'Home' });
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../variables.scss';

.header {
  height: 120px;
  width: 100%;
  cursor: pointer;

  .header__left {
    position: relative;
    flex: 1 0 auto;
    height: 100%;

    img {
      height: 100px;
      width: auto;
      transform: rotate(20deg);
      margin-left: 20px;

      @media (max-width: 768px) {
        height: 50px;
      }
    }

    h1 {
      display: inline-block;
      margin-left: 30px;
      font-size: 45px;
      font-weight: bold;
      color: $white;

      @media (max-width: 768px) {
        font-size: 22px;
      }
    }

    .header__left_svg {
      position: absolute;
      top: 85px;
      left: 320px;

      @media (max-width: 768px) {
        display: none;
      }
    }
  }

  .header__right {
    flex: 1 0 auto;
    height: 100%;

    h4 {
      display: inline-block;
      margin-right: 30px;
      font-size: 25px;
      font-weight: bold;
      color: $white;
      cursor: pointer;

      @media (max-width: 768px) {
        font-size: 16px;
      }
    }
  }
}
</style>
