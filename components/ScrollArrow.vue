<template>
  <div>
    <v-icon :size="height" class="scroll-icon" @click="$vuetify.goTo(target)"
      >mdi-arrow-down</v-icon
    >
  </div>
</template>

<style lang="scss" scoped>
$animation-offset: 30px;

.scroll-icon {
  animation: 2s 5s infinite movearrow, 2s ease-out fadein 2s forwards;
  opacity: 0;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

// TODO Améliorer l'animation
@keyframes movearrow {
  0% {
    top: 0px;
  }
  12.5% {
    top: $animation-offset;
  }
  25% {
    top: 0px;
  }
  37.5% {
    top: $animation-offset;
  }
  // On divise l'animation en 2 parties pour qu'elle puisse se pauser.
  50% {
    top: 0px;
  }
  100% {
    top: 0px;
  }
}
</style>

<script>
export default {
  props: {
    height: String,
    target: {
      type: String,
      default: '#content',
    },
  },
}
</script>