<template>
  <q-drawer show-if-above side="left" bordered :width="200">
    <q-scroll-area class="fit">
      <!-- แสดงเมนูในแต่ละหน้า -->
      <q-list bordered>
        <q-item-label header> รายการในแต่ละหน้า </q-item-label>
        <template v-for="(menuItem, index) in menuList" :key="index">
          <q-item
            clickable
            v-ripple
            tag="a"
            :to="menuItem.to"
            :exact="menuItem.exact"
          >
            <q-item-section avatar>
              <q-icon :name="menuItem.icon" />
            </q-item-section>
            <q-item-section>{{ menuItem.Label }}</q-item-section>
          </q-item>
        </template>
      </q-list>
    </q-scroll-area>
  </q-drawer>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

const menuList = [
  {
    icon: 'home',
    Label: 'Home',
    separator: true,
    to: '/',
    exact: true,
  },
  {
    icon: 'article',
    Label: 'About',
    separator: true,
    to: '/about',
  },
  {
    icon: 'contacts',
    Label: 'Contact',
    separator: true,
    to: '/contact',
  },
];

export default defineComponent({
  name: 'DrawerComponent',
  setup() {
    return {
      miniState: ref(false),
      menuList,
    };
  },
  // methods: {
  //   handleItemClick(menuItem) {
  //     console.log(menuItem.route);
  //   },
  // },
});
</script>
