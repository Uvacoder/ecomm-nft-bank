<template>
  <div>
    <div>
      <h1
      >
        All Tags
      </h1>
    </div>
    <ul>
      <li v-for="tag in tags" :key="tag" class="text-center mb-2">
        <nuxt-link
          :to="{ name: 'tags-tag', params: { tag: tag.toLowerCase() } }"
          class="text-4xl hover:underline"
          >{{ tag }}</nuxt-link
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TagListPage',
  layout: 'PageLayout',
  async asyncData({ $content }) {
    function onlyUnique(value, index, self) {
      return self.indexOf(value) === index;
    }
    const articles = await $content('articles').only(['tags']).fetch();
    const tags = articles.flatMap((article) => article.tags).filter(onlyUnique);
    return {
      tags,
    };
  },
  head() {
    return {
      title: 'Article Tags - Learning Laravel and VueJS',
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: `${this.$config.baseUrl}/tags`,
        },
      ],
    };
  },
};
</script>
