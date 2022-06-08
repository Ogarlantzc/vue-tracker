<template>
  <el-button default-active="1">
    <el-button-icons
      @click="sendCopyTaskname"
      class="icon"
      size="medium"
      index="1"
    >
      <Copie />
    </el-button-icons>
    <el-button-icons @click="sendRestart" class="icon" index="2">
      <Search />
    </el-button-icons>
    <el-button-icons @click="sendDelete" class="icon" index="3">
      <Delete /> </el-button-icons
  ></el-button>
</template>
<script>
import Copie from "./icons/Copie.vue";
import Search from "./icons/Search.vue";
import Delete from "./icons/Delete.vue";

export default {
  components: {
    Copie,
    Search,
    Delete,
  },
  props: {
    taskID: {
      type: String,
      required: true,
    },
  },
  emits: ["restart", "delete", "copyTaskname"],
  methods: {
    sendRestart() {
      this.$emit("restart", this.taskID);
    },
    sendDelete() {
      this.$emit("delete", this.taskID);
    },
    sendCopyTaskname() {
      this.$emit("copyTaskname");
    },
  },
};
</script>

<style scoped>
.el-button {
  border: none;
}
.icon {
  padding: 1rem;
}
</style>