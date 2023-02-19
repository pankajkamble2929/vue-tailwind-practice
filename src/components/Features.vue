<template>
  <div class="mt-20 flex flex-row">
    <div class="w-1/3 bg-gray-100">
      <button
        v-for="(tab, index) in tabs"
        :key="index"
        @click="openTab(tab)"
        :class="{ 'bg-gray-300': activeTab === tab }"
        class="w-full text-left px-4 py-2 border-gray-200 hover:bg-gray-200 focus:outline-none"
      >
        {{ tab }}<br>
        <span class="text-sm text-gray-600">{{ descriptions[tab] }}</span>
      </button>
    </div>
    <div class="w-2/3 p-4">
      <div v-for="(tab, index) in tabs" :key="index" v-show="activeTab === tab">
        <h3 class="text-xl font-bold">{{ tab }}</h3>
        <img :src="images[tab]" :alt="`${tab} Image`" class="my-4">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabs: ['London', 'Paris', 'Tokyo'],
      activeTab: 'London',
      descriptions: {
        London: 'London is the capital city of England.',
        Paris: 'Paris is the capital of France.',
        Tokyo: 'Tokyo is the capital of Japan.',
      },
      images: {
        London: 'https://cdn.pixabay.com/photo/2018/04/11/09/38/london-3316703_960_720.jpg',
        Paris: 'https://cdn.pixabay.com/photo/2017/08/07/08/08/paris-2590608_960_720.jpg',
        Tokyo: 'https://cdn.pixabay.com/photo/2018/04/03/02/11/tokyo-3281746_960_720.jpg',
      },
    };
  },
  methods: {
    openTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style>
/* No CSS needed thanks to Tailwind! */
</style>
