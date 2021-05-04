<template>
  <div class="container">
    <b-navbar class="navbar is-size-6 is-size-5-mobile">
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '#' }">
          <img src="https://easycrypto.ai/img/logo-200px.png" class="navbar-brand navbar-item logo" alt="">
        </b-navbar-item>
      </template>
      <template #end>
        <b-navbar-dropdown label="Buy & Sell">
          <b-navbar-item href="#">
            Instance buy and sell
          </b-navbar-item>
          <b-navbar-item href="#">
            Multi-coin oder
          </b-navbar-item>
          <b-navbar-item href="#">
            Auto-buy
          </b-navbar-item>
          <b-navbar-item href="#">
            Swap
          </b-navbar-item>
          <b-navbar-item href="#">
            Pro trading
          </b-navbar-item>
          <b-navbar-item href="#">
            Hardware wallet
          </b-navbar-item>
        </b-navbar-dropdown>
        <b-navbar-item href="#" active>
          Rates
        </b-navbar-item>
        <b-navbar-item href="#">
          Tracker
        </b-navbar-item>
        <b-navbar-item href="#">
          About Us
        </b-navbar-item>
        <b-navbar-item href="#">
          Tracker
        </b-navbar-item>
        <b-navbar-item href="#">
          Log in
        </b-navbar-item>
        <b-navbar-item>
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
        </b-navbar-item>
      </template>
    </b-navbar>
  </div>
</template>
<script>
export default {

}
</script>
