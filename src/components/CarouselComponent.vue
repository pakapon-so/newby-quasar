<template>
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      navigation
      infinite
      :autoplay="autoplay"
      arrows
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
      <!-- วนลูปรูปภาพที่รับมา IndexPage.vue -->
      <q-carousel-slide
        v-for="(item, index) in items"
        :key="index"
        :name="item.name"
        :img-src="item.imgSrc"
      />
    </q-carousel>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType, ref } from 'vue';

export default defineComponent({
  name: 'CarouselComponent',
  // รับค่า items มาจาก IndexPage.vue โดยใช้ props และกำหนด type เป็น Array ของ Object ที่มี key ชื่อ name และ imgSrc และกำหนดค่าเริ่มต้นเป็น [] หรือ Array ว่าง
  props: {
    items: {
      type: Array as PropType<{ name: number; imgSrc: string }[]>,
      required: true,
    },
  },
  setup() {
    const slide = ref(1);
    const autoplay = ref(true);
    return { slide, autoplay };
  },
});
</script>
