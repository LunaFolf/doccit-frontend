<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <q-page padding>
        <router-view />
        <div class="menuBtnDiv" :class="{active: menuOpen}">
          <q-btn
            round
            color="accent"
            size="lg"
            class="menuBtn"
            @click="menuOpen = !menuOpen"
          >
            <q-img :src="require('assets/Doccit White.svg')" class="q-ma-xs" />
          </q-btn>
          <div class="menuBtns" :class="{active: menuOpen}">
            <q-btn color="red" icon="dashboard" round class="option-1" />
            <q-btn color="red" icon="dashboard" round class="option-2" />
            <q-btn color="red" icon="dashboard" round class="option-3" />
            <!-- <q-btn color="red" icon="dashboard" round /> -->
            <!-- <q-btn color="red" round /> -->
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>
<script>
export default {
  data () {
    return {
      menuOpen: false
    }
  }
}
</script>
<style lang="stylus">
.menuBtnDiv
  position absolute
  left 18px
  bottom 18px
  transition transform .5s
  transform-origin 30px 30px
  transform rotate(-90deg)
  &.active
    transform rotate(0)

  .menuBtns
    display none
    &.active
      display block
    .q-btn
      position absolute
    .option-1
      left calc(50% - 20px)
      bottom 12em
    .option-2
      left 7.5em
      bottom 7.5em
    .option-3
      left 12em
      bottom calc(50% - 20px)

</style>
