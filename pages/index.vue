<template>
  <div class="flex-grow">
    <div class="container mx-auto">
      <div class="grid grid-cols-2 gap-4">
        <div class="container mx-auto">
          <div class="text-xl">Raffil using system time</div>
          <div>{{ machineTime }}</div>
        </div>

        <div class="container mx-auto">
          <div class="text-xl">Raffil using server time</div>
          <div class="text-lg">Binance: GET https://api.binance.com/api/v3/time</div>
          <div>{{ timestamp }}</div>
        </div>
      </div>
    </div>
    <footer>
      <NuxtLink to="/about">About Page</NuxtLink>
    </footer>
  </div>
</template>

<script>
export default {
  layout: "mainLayout",
  name: "IndexPage",
  data() {
    return {
      timestamp: "",
      machineTime: "",
    };
  },
  async mounted() {
    setInterval(() => {
      this.machineTime = new Date(Date.now());
    }, 1000);
    let url = "https://api.binance.com/api/v3/time";
    await this.$http.$get(url).then((response) => {
      console.log("GOT RESPONSE");
      console.log(response);
      let time = response.serverTime;
      var date = new Date(time);
      console.log(date);
      this.timestamp = date;
    });
  },
};
</script>
