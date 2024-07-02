<template>
  <!-- สร้าง Carousel หรือ ภาพเลื่อน -->
  <q-page padding>
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
        <q-carousel-slide
          :name="1"
          img-src="https://cdn.quasar.dev/img/mountains.jpg"
        />
        <q-carousel-slide
          :name="2"
          img-src="https://cdn.quasar.dev/img/parallax1.jpg"
        />
        <q-carousel-slide
          :name="3"
          img-src="https://cdn.quasar.dev/img/parallax2.jpg"
        />
        <q-carousel-slide
          :name="4"
          img-src="https://cdn.quasar.dev/img/quasar.jpg"
        />
      </q-carousel>
    </div>

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
      <card-component title="finance" subtitle="by Doe Dee">
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
import { ref } from 'vue';

const slide = ref(1);
const autoplay = ref(true);

defineOptions({
  name: 'IndexPage',
  components: {
    CardComponent,
  },
});
</script>
