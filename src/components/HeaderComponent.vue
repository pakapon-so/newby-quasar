<template>
  <div class="q-pa-md q-gutter-y-sm">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="$emit('openDrawer')" />
        <q-toolbar-title class="text-center q-ma-sm">
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          &nbsp;&nbsp;&nbsp; ห้องสมุด by KST
        </q-toolbar-title>
        <!-- <q-input v-model="text" class="q-ma-sm" dense standout dark>
          <template v-slot:append>
            <q-icon name="search" />
          </template>
        </q-input> -->
      </q-toolbar>
    </q-header>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
export default defineComponent({
  name: 'HeaderComponent',
  setup() {
    return {
      text: ref(''),
    };
  },
});
</script>
