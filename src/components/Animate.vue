<template>
  <div>
    <div @click="show=!show">show</div>
    <transition name="fade">
        <p v-show="show" v-bind:style="styleobj">hahahaha</p>
    </transition>
  </div>
</template>
<script>
export default{
  name: 'Animates',
  mounted: function () {
    console.log('monted1')
  },
  data: function () {
    return {
      show: true,
      styleobj: {
        fontSize: '30px',
        color: 'red'
      }
    }
  }
}
</script>
<style scoped>
  .fade-enter-active{
    transition:all 1.1s ease;
    font-size:20px;
    color:green;
  }
  .fade-enter,.fade-leave-to{
    transform1: translateX(10px);
    font-size:10px;
    color:yellow;
  }
  .fade-leave-active{
    transition:all 1.38s ease;
    font-size:30px;
    color:green;
  }
</style>
