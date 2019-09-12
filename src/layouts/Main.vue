<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <q-page padding>
        <router-view />
        <q-page-sticky position="bottom-left" :offset="[18, 18]">
          <q-btn
            round
            color="accent"
            size="lg"
            icon="menu"
            @click="drawer = !drawer"
          />
        </q-page-sticky>
      </q-page>
    </q-page-container>
  </q-layout>
</template>
<script>
export default {

}
</script>
<style lang="stylus">

</style>
