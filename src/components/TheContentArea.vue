<template>
  <div class="h-screen relative">
    <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
      <slot>

      </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheContentCard',
};
</script>
