<template>
  <div class="counter q-gutter-y-md">
    <q-btn
      class="full-width"
      color="primary"
      size="xl"
      :label="counter"
      @click.stop="increment"
    />
    <div class="flex items-center justify-between">
      <q-btn
        flat
        round
        color="negative"
        size="lg"
        icon="remove"
        @click.stop="decrement"
      />
      <q-btn
        flat
        round
        color="black"
        size="lg"
        icon="restart_alt"
        @click.stop="reset"
      />
      <q-btn
        flat
        round
        color="positive"
        size="lg"
        icon="add"
        @click.stop="increment"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const counter = ref(0);

const increment = () => {
  counter.value += 1;
};

const decrement = () => {
  if (counter.value > 0) {
    counter.value -= 1;
  }
};

const reset = () => {
  counter.value = 0;
};
</script>
