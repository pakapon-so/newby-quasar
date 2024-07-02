<template>
  <q-page padding>
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

defineOptions({
  name: 'IndexPage',
  components: {
    CardComponent,
  },
});
</script>
