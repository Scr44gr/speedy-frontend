<template>
  <c-theme-provider>
    <c-reset />
    <Main></Main>
  </c-theme-provider>
</template>

<script>
import Main from './views/Main.vue';
export default {
  name: "App",
  components: {
    Main,
  },
};
</script>
