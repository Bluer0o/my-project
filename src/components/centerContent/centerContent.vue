<template>
  <div class="content_right">
    <topCardVue class="topCardVue" />
    <contentFormVue class="contentFormVue" />
  </div>
</template>

<script>
import contentFormVue from "./contentForm.vue";
import topCardVue from "./topCard.vue";

export default {
  components: {
    contentFormVue,
    topCardVue,
  },
};
</script>

<style>
.content_right {
  /* width: 1164px; */
  overflow: hidden;
}
.topCardVue {
  height: 188px;
}
.topCardVue,
.contentFormVue {
  background: #fff;
  border-radius: 8px;
  /* width: calc(100% - 110px); */
  margin: 24px 24px 0px 24px;
}
</style>