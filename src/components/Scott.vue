<template>
  <div>
    <scott-comp-1 />
    <scott-comp-2 />
    <scott-comp-3 />
    <scott-comp-4 />
    <scott-comp-5 />
    <scott-comp-6 />
    <scott-comp-7 />
    <scott-comp-8 />
    <scott-comp-9 id="3" />
    <scott-comp-9 id="5" />
    <scott-comp-9 id="7" />
  </div>
</template>

<script>
import ScottComp1 from "./Scott/ScottComp1";
import ScottComp2 from "./Scott/ScottComp2";
import ScottComp3 from "./Scott/ScottComp3";
import ScottComp4 from "./Scott/ScottComp4";
import ScottComp5 from "./Scott/ScottComp5";
import ScottComp6 from "./Scott/ScottComp6";
import ScottComp7 from "./Scott/ScottComp7";
import ScottComp8 from "./Scott/ScottComp8";
import ScottComp9 from "./Scott/ScottComp9";

export default {
  name: "App",
  components: {
    ScottComp1,
    ScottComp2,
    ScottComp3,
    ScottComp4,
    ScottComp5,
    ScottComp6,
    ScottComp7,
    ScottComp8,
    ScottComp9,
  },
};
</script>

<style>
</style>
