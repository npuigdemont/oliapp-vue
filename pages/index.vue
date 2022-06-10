<template>
  <div>
    <Navigation />
    <main>
     
      <Carrousell />
    </main>
  </div>
</template>

<script>
import Carrousell from "../components/Carrousell.vue";
import Announcement from "../components/Announcement.vue";
import Navigation from "../components/Navigation.vue";
export default {
    name: "IndexPage",
    components: { Carrousell, Announcement, Navigation }
}
</script>
<style>

</style>