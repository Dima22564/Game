<template>
  <button class="button" :class="'button_' + color">{{ label }}</button>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="sass">
  @import 'theme/_vars'
  @import 'theme/_mix'
  .button
    background: none
    border: none
    outline: none
    font-size: 14px
    line-height: 16px
    padding: 12px 32px
    border-radius: 6px
    color: $white
    font-weight: 500
    cursor: pointer
    +md
      padding: 8px 34px
    &_primary
      background: dark-blue(1)
      transition: all 0.1s
      &:hover
        background: rgba(136, 117, 255, 1)
</style>
