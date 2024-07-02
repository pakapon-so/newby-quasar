<template>
  <div class="col-md-4 col-12">
    <q-card class="my-card">
      <q-card-section>
        <div class="text-h6">{{ title }}</div>
        <div class="text-subtitle2">{{ subtitle }}</div>
      </q-card-section>
      <q-card-section>
        <slot></slot>
      </q-card-section>
    </q-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'CardComponent',
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
    },
  },
});
</script>
