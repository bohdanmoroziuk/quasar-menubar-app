<template>
  <q-page class="q-pa-md">
    <counter />
    <q-btn
      class="absolute-bottom-right"
      color="black"
      size="sm"
      icon="power_settings_new"
      flat
      round
      @click.stop="quit"
    />
  </q-page>
</template>

<script setup lang="ts">
import Counter from 'src/components/Counter.vue';

const quit = () => {
  window.system.quitApp();
};
</script>
