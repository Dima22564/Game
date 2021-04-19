<template>
  <header class="auth-header">
    <b-container>
      <div class="auth-header__main">
        <nuxt-link class="auth-header__logo" to="/">
          <img src="/images/logo.svg" alt="">
        </nuxt-link>

        <main-button color="primary" label="Регистрация" />
      </div>
    </b-container>
  </header>
</template>

<script>
import MainButton from '~/components/MainButton'
export default {
  name: 'AuthTopMenu',
  components: { MainButton }
}
</script>

<style lang="sass">
  @import 'theme/_vars'
  @import 'theme/_mix'
  .auth-header
    background: rgba(41, 37, 56, 1)
    &__main
      display: flex
      align-items: center
      justify-content: space-between
      padding: 22px 0
    &__logo
      +md
        max-width: 103px
      img
        width: 100%
</style>
