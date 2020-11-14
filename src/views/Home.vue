<template>
  <div class="container">
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ColumnList, { ColumnProps } from "../components/ColumnList.vue";
const testData: ColumnProps[] = [
  {
    id: 1,
    title: "专栏1",
    description:
      "l 号：猫共有三条腿命题2 号：石头是没有生命的命题3 号：太阳的形状是三角形命题4 号：",
    avatar: "https://cdn.novenn.com/random/images/2020-05-12.jpg",
  },
  {
    id: 2,
    title: "专栏2",
    description:
      "l 号：猫共有三条腿命题2 号：石头是没有生命的命题3 号：太阳的形状是三角形命题4 号：",
    avatar: "https://cdn.novenn.com/random/images/2020-05-12.jpg",
  },
  {
    id: 3,
    title: "专栏3",
    description:
      "l 号：猫共有三条腿命题2 号：石头是没有生命的命题3 号：太阳的形状是三角形命题4 号：",
    avatar: "https://cdn.novenn.com/random/images/2020-05-12.jpg",
  },
  {
    id: 4,
    title: "专栏4",
    description:
      "l 号：猫共有三条腿命题2 号：石头是没有生命的命题3 号：太阳的形状是三角形命题4 号：",
    avatar: "https://cdn.novenn.com/random/images/2020-05-12.jpg",
  },
];

export default defineComponent({
  name: "Home",
  components: { ColumnList },
  setup() {
    return {
      list: testData,
    };
  },
});
</script>
