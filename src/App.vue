<template>
  <div id="app" class="bg-cover bg-center bg-scroll" :style="{ backgroundImage: 'url(' + require('@/assets/bg/zuzu_wide_pink_rev_high.jpg') + ')' }">
      <the-content-area>
        <base-card>
          <the-main-logo/>
          <links-card/>
        </base-card>
      </the-content-area>
  </div>
</template>

<script>
import BaseCard from '@/components/BaseCard';
import TheContentArea from '@/components/TheContentArea';
import TheMainLogo from '@/components/TheMainLogo';
import LinksCard from '@/components/LinksCard';

export default {
  name: 'App',
  components: {
    BaseCard, TheContentArea, TheMainLogo, LinksCard
  },
  data() {
    return {
      image: '@/assets/zuzu_wide_pink_rev_high.jpg',
    };
  },
};
</script>
