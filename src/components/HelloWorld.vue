<template>
  <div>
    <headerMenuVue class="header" />
    <div class="content">
      <leftMenuVue class="leftMenuVue" />
      <centerContentVue />
    </div>
  </div>
</template>
<script>
import centerContentVue from "./centerContent/centerContent.vue";
import headerMenuVue from "./headerMenu/headerMenu.vue";
import leftMenuVue from "./leftMenu/leftMenu.vue";

export default {
  components: {
    headerMenuVue,
    leftMenuVue,
    centerContentVue,
  },
};
</script>

<style>
.header {
  position: fixed;
  width: 100%;
  z-index: 999;
}
.leftMenuVue {
  height: 100%;
  background: #fff;
}
.content {
  display: flex;
  padding-top: 48px;
}
</style>