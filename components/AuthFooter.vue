<template>
  <footer class="footer footer__auth">
    <b-container>
      <div class="footer__wrapper">
        <span class="footer__text">© Gameincome 2021</span>
        <nuxt-link class="footer__text" tag="span" to="/">Политика конфиденциальности</nuxt-link>
        <span class="footer__text">made by <span class="footer__text footer__text_white">roob.in</span></span>

        <div class="footer__socials">
          <CustomIcon :size="40" class="footer__social" :is-link="true" to="/" >
            <template slot="icon">
              <img src="/images/vk.svg" alt="">
            </template>
          </CustomIcon>

          <CustomIcon :size="40" class="footer__social" :is-link="true" to="/" >
            <template slot="icon">
              <img src="/images/fb.svg" alt="">
            </template>
          </CustomIcon>

          <CustomIcon :size="40" class="footer__social" :is-link="true" to="/" >
            <template slot="icon">
              <img src="/images/inst.svg" alt="">
            </template>
          </CustomIcon>
        </div>
      </div>
    </b-container>
  </footer>
</template>

<script>
import CustomIcon from '~/components/CustomIcon'
export default {
  name: 'AuthFooter',
  components: { CustomIcon }
}
</script>

<style lang="sass">
  @import 'theme/_vars'
  @import 'theme/_mix'
  .footer
    background: #292538
    &__socials
      display: flex
      align-items: center
      +md
        margin-top: 16px
    &__social
      &:not(:last-child)
        margin-right: 20px
    &__wrapper
      display: flex
      align-items: center
      justify-content: space-between
      +md
        flex-direction: column
        align-items: flex-start
    &__auth
      padding: 12px 0
      +md
        padding: 24px 0 20px
    &__text
      letter-spacing: -0.4px
      font-size: 14px
      line-height: 20px
      color: $gray
      +lg
        line-height: 18px
        &:not(:last-child)
          margin-bottom: 8px
      &_white
        color: $white

</style>
