<template>
  <q-layout view="hhh LpR fff">
    <!-- header -->
    <HeaderComponent @openDrawer="toggleLeftDrawer" />
    <!-- @openDrawer รับสัญญาณจากการกดปุ่ม Drawer ใน HeaderComponent-->

    <!-- DrawerComponent -->
    <DrawerComponent v-model="leftDrawerOpen" />

    <!-- ส่วนเนื้อหา -->
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- footer  -->
  </q-layout>
</template>

<script>
import { ref } from 'vue';
import HeaderComponent from 'components/HeaderComponent.vue';
import DrawerComponent from 'components/DrawerComponent.vue';

export default {
  setup () {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        // ฟังก์ชันเปิด-ปิดเมนู Drawer
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
  components: {
    HeaderComponent,
    DrawerComponent,
  },
  mounted() {
    // ฟังก์ชันที่ทำงานหลังจากที่ component ถูก render
    this.leftDrawerOpen = false;
  },
};
</script>
