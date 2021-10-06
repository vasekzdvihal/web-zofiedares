<template>
  <div class="justify-center flex">
    <div class="container shadow-lg rounded-xl border border-gray-800 m-1 p-1 md:w-2/3 bg-gray-800 bg-opacity-25">
      <ul class="flex flex-row justify-center">
        <li
          v-for="media in socialMedias"
          :key="media.id"
          class="items-center flex"
        >
          <a :href="media.url">
            <div class="w-14 container flex">
              <img
                class="p-2"
                :src="require('@/assets/icon/' + media.icon)"
              >
            </div>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LinksCard',
  data() {
    return {
      socialMedias: [
        {
          id: 1,
          label: 'Facebook',
          icon: 'facebook-square-brands.svg',
          url: 'https://www.facebook.com/zofiedares/',
        },
        {
          id: 2,
          label: 'Instagram',
          icon: 'instagram-brands.svg',
          url: 'https://www.instagram.com/zofiedares/',
        },
        {
          id: 3,
          label: 'YouTube',
          icon: 'youtube-brands.svg',
          url: 'https://www.youtube.com/channel/UCCePfCFdhm9mr4OII3WgmHQ',
        },
        {
          id: 4,
          label: 'Spotify',
          icon: 'spotify-brands.svg',
          url: 'https://open.spotify.com/artist/1TTYqDeHwR0tarujudGxsK',
        },
        {
          id: 5,
          label: 'Apple Music',
          icon: 'apple-brands.svg',
          url: 'https://music.apple.com/gb/album/high-on-being-ep/1448257217',
        },
      ],
    };
  },
};
</script>

<style scoped>

</style>
