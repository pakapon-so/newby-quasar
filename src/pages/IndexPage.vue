<template>
  <q-page padding>
    <!-- สร้าง Carousel หรือ ภาพเลื่อน -->
    <carousel-component :items="carouselItems" />

    <!-- แสดง Card -->
    <div class="row q-col-gutter-md">
      <card-component title="Our Changing Planet" subtitle="by John Doe">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Neque eveniet
        quod eos facere, cumque rem a
      </card-component>
      <card-component title="Hightech" subtitle="by Hex Dee">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt rerum
        dolorem officiis molestiae assumenda dolore ab itaque, molestias modi
        sapiente sunt iste, quod velit doloremque incidunt fugiat quasi quaerat
        libero.
      </card-component>
      <card-component title="finance">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita a ipsa
        explicabo officia delectus aspernatur, laudantium aperiam nostrum
        asperiores quidem. Doloremque harum eaque, assumenda quis saepe
        accusantium voluptas omnis earum.
      </card-component>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import CardComponent from 'src/components/CardComponent.vue';
import CarouselComponent from 'src/components/CarouselComponent.vue';
import { ref } from 'vue';

const carouselItems = ref([
  { name: 1, imgSrc: 'https://cdn.quasar.dev/img/mountains.jpg' },
  { name: 2, imgSrc: 'https://cdn.quasar.dev/img/parallax1.jpg' },
  { name: 3, imgSrc: 'https://cdn.quasar.dev/img/parallax2.jpg' },
  { name: 4, imgSrc: 'https://cdn.quasar.dev/img/quasar.jpg' },
]);

defineOptions({
  name: 'IndexPage',
  components: {
    CardComponent,
    CarouselComponent,
  },
});
</script>
