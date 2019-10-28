<template>
  <div>
    <Start />
    <Clinic />
    <Pricing />
    <Team />
    <Blog />
  </div>
</template>

<script>
import Start from "@/components/layoutComponents/Start";
import Clinic from "@/components/layoutComponents/Clinic";
import Team from "@/components/layoutComponents/Team";
import Pricing from "@/components/layoutComponents/Pricing";
import Blog from "@/components/layoutComponents/Blog";
export default {
  components: { Start, Clinic, Team, Pricing, Blog }
};
</script>

<style lang="scss">
</style>
