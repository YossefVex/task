<template>
  <div class="tree">
    <ul class="nav first">
      <node-tree :node="treeData"></node-tree>
    </ul>
  </div>
</template>

<script>
import NodeTree from "./components/NodeTree";

export default {
  props: {
    treeData: Object,
  },
  components: {
    NodeTree,
  },
};
</script>

<style>
</style>
