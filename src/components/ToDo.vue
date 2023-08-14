<template>
  <li>{{ toDo }} <button @click="removeThisToDo">Remove this Todo</button></li>
</template>

<script>
export default {
  props: ["toDo"],
  methods: {
    removeThisToDo() {
      this.$emit("removeThisToDo", this.toDo);
    },
  },
};
</script>
