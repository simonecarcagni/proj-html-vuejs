<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';
import PreHeader from './components/PreHeader.vue';
export default {
  components: {
    MyHeader,
    MyMain,
    MyFooter,
    PreHeader,
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <PreHeader />
  <MyHeader />
  <MyMain />
  <MyFooter />
</template>

<style lang="scss">
@use './styles/general.scss';
@use './styles/partials/variable' as *;
</style>
