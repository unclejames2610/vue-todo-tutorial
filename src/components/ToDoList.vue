<template>
  <ul>
    <ToDo
      v-for="(item, itemIndex) in myProp"
      :key="itemIndex"
      :toDo="item"
      @removeThisToDo="sendTheMessage"
    />
    {{
      item
    }}
  </ul>
</template>

<script>
import ToDo from "./ToDo.vue";
export default {
  components: {
    ToDo,
  },
  //   props: {
  //     myProp: {
  //       type: Array,
  //       default: () => [],
  //     },
  //   },
  props: ["myProp"],
  methods: {
    // removeList() {
    //   this.$emit("removeList");
    // },
    sendTheMessage(toDo) {
      console.log(toDo);
      this.$emit("removeToDo", toDo);
    },
  },
};
</script>
