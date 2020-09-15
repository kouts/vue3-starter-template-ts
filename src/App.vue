<template>
  <div id="app">
    <component :is="layout">
      <router-view />
    </component>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import '@/scss/app.scss';

export default defineComponent({
  computed: {
    layout() {
      return `layout-${this.$route.meta.layout || 'default'}`;
    }
  }
});
</script>
