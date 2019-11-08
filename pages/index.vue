<template>
  <div class="wrapper">
    <Start />
    <Booking />
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
import Booking from "@/components/layoutComponents/Booking";
export default {
  components: { Start, Clinic, Team, Pricing, Blog, Booking }
};
</script>

<style lang="scss">
.wrapper {
  width: 100%;
  height: auto;
  flex-flow: column wrap;
  align-items: center;
  justify-content: center;
}
</style>
