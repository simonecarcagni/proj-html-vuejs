<script>
import PreHeader from './components/PreHeader.vue';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';
import PostFooter from './components/PostFooter.vue';
export default {
  components: {
    PreHeader,
    MyHeader,
    MyMain,
    MyFooter,
    PostFooter
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
  <PostFooter />
</template>

<style lang="scss">
@use './styles/general.scss';
@use './styles/partials/variable' as *;
</style>
