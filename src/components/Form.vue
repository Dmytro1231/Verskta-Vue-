<template>
  <div class="container">
    <UserLocation />
  </div>
</template>

<script>
import UserLocation from "@/components/UserLocation";
export default {
  components: {
    UserLocation,
  },
};
</script>

<style lang="scss" scoped>
.container {
  background: url("../assets/bg-header.png") no-repeat 100% 100%;
  background-size: cover;
  padding-top: 60px;
  padding-bottom: 60px;
}
@media (max-width: 320px) {
  .container {
    .title {
      font-size: 20px !important;
      width: 290px;
    }
  }
}
</style>