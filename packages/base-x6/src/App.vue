<script setup>
import { onMounted } from "vue";
import { Graph } from "@antv/x6";

onMounted(() => {
  const graph = new Graph({
    container: document.getElementById("container"),
    grid: true,
  });

  const source = graph.addNode({
    x: 40,
    y: 40,
    width: 100,
    height: 40,
    label: "Hello",
  });

  const target = graph.addNode({
    x: 160,
    y: 160,
    width: 100,
    height: 40,
    label: "World",
  });

  graph.addEdge({
    source,
    target,
  });
});
</script>

<template>
  <div>
    <div id="container" style="width: 500px; height: 500px"></div>
  </div>
</template>

<style scoped></style>
