<template>
  <el-menu default-active="1">
    <h3>Vue Tracker</h3>
    <el-menu-item index="1">
      <Clock />
      <span>Tracker</span>
    </el-menu-item>
    <el-menu-item index="2" disabled>
      <Category />
      <span>Catégories</span>
    </el-menu-item>
    <el-menu-item index="3" disabled>
      <Setting />
      <span>Paramètres</span>
    </el-menu-item>
  </el-menu>
</template>

<script>
import Clock from "./icons/Clock.vue";
import Category from "./icons/Category.vue";
import Setting from "./icons/Setting.vue";

export default {
  components: {
    Clock,
    Category,
    Setting,
  },
};
</script>

<style scoped>
.el-menu {
  border-right: none;
  text-align: left;
}

h3 {
  text-align: center;
}
</style>