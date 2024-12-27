<template>
  <p class="font-[gt] text-[14px]" data-cursor="-icon" id="time_span"></p>
</template>

<script>
export default {
  methods: {},

  mounted() {
    timer();

    function timer() {
      var currentTime = new Date();
      var hours = currentTime.getHours();
      var minutes = currentTime.getMinutes();
      
      if (minutes < 10) {
        minutes = "0" + minutes;
      }
      var t_str = hours + ":" + minutes + " ";
      if (hours > 11) {
        t_str += "PM";
      } else {
        t_str += "AM";
      }
      document.getElementById("time_span").innerHTML = t_str;
      setTimeout(timer, 1000);
    }
  },
};
</script>

<style></style>
