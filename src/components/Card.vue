<template>
  <div class="card">
    <img :src="data?.image" class="card-img-top" :alt="data?.text" />
    <div class="card-body">
      <p class="card-text">
        {{ data?.text }}
      </p>
      <a href="#" class="card__action">Read More</a>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { Card } from "./types";

defineProps<{
  data: Card;
}>();
</script>

<style lang="stylus" scoped>
.card
  max-width 300px
  min-height 100%
  transition 0.3s
  margin 0 auto
  &:hover
    box-shadow 2px -2px 3px #eaeaea
  &-text
    text-align center
  &__action
    border 3px solid #000
    text-transform uppercase
    border-radius 100px
    text-align center
    font-weight bold
    color #000
    text-decoration none
    letter-spacing 2px
    padding 8px 30px
    width max-content
    align-self center
    transition 0.3s
    &:hover
      background #000
      color #fff
  &-body
    display flex
    flex-direction column
    justify-content space-between
  &-img
    &-top
      padding 1rem
      border-radius 25px !important
</style>
