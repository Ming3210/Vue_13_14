<template>
  <div>
    <h1>B4</h1>
    <v-menu>
      <template v-slot:activator="{ props }">
        <v-btn color="primary" v-bind="props"> Quản trị viên </v-btn>
      </template>
      <v-list>
        <v-list-item v-for="(item, index) in items" :key="index" :value="index">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script setup>
const items = [
  { title: "Thông tin cá nhân" },
  { title: "Đổi mật khẩu" },
  { title: "Đăng xuất" },
];
</script>

<style></style>
