<template>
  <nav class="navbar navbar-dark bg-primary justify-content-between mb-4 px-2">
    <a href="#" class="navbar-brand">知乎专栏</a>
    <ul v-if="!userInfo.isLogin" class="list-inline mb-0">
      <li class="list-inline-item">
        <a href="#" class="btn btn-outline-light my-2">登录</a>
      </li>
      <li class="list-inline-item">
        <a href="#" class="btn btn-outline-light my-2">注册</a>
      </li>
    </ul>
    <ul v-else class="list-inline mb-0">
      <li class="list-inline-item">
        <dropdown :title="`你好,${userInfo.name}`">
          <dropdown-item>
            <a href="#" class="dropdown-item">新建文章</a>
          </dropdown-item>
          <dropdown-item disabled>
            <a href="#" class="dropdown-item">编辑资料文章</a>
          </dropdown-item>
          <dropdown-item>
            <a href="#" class="dropdown-item">退出登录</a>
          </dropdown-item>
        </dropdown>
        <!-- <a href="#" class="btn btn-outline-light my-2">{{ userInfo.name }}</a> -->
      </li>
    </ul>
  </nav>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import Dropdown from "./Dropdown.vue";
import DropdownItem from "./DropdownItem.vue";
export interface UserProps {
  isLogin: boolean;
  name?: string;
  id?: number;
}
export default defineComponent({
  name: "GlobalHeader",
  components: { Dropdown, DropdownItem },
  props: {
    user: {
      type: Object as PropType<UserProps>,
      required: true,
    },
  },
  setup(props) {
    return {
      userInfo: props.user,
    };
  },
});
</script>

<style scoped>
</style>