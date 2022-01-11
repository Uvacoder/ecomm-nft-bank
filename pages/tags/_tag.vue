<template>
  <div> 
    <h1 
      >
        #{{ $route.params.tag.toUpperCase() }}
      </h1>
    <ArticleList :articles="articlesByTag" />
  </div>
</template>
<style>
  h1 {
    background-color: snow;
    color: rebeccapurple;
    margin: auto;
    padding: 0.5em; 
    text-align: center; 
  }
</style>
<script>
import ArticleList from '@/components/ArticleList';

export default {
  name: 'TagPage',
  layout: 'PageLayout',
  components: {
    ArticleList,
  },
  async asyncData({ $content, params }) {
    const articles = await $content('articles')
      .only(['title', 'description', 'image', 'slug', 'published', 'tags', 'author'])
      .sortBy('published', 'desc')
      .fetch();
    const articlesByTag = articles.filter((article) => {
      const articleTags = article.tags.map((x) => x.toLowerCase());
      return articleTags.includes(params.tag);
    });
    return {
      articlesByTag,
    };
  },
  methods: {
    captialise(text) {
      return text.charAt(0).toUpperCase() + text.slice(1);
    },
  },
  head() {
    return {
      title: `Articles Tagged - ${this.captialise(this.$route.params.tag)}`,
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: `${this.$config.baseUrl}/tags/${this.$route.params.tag}`,
        },
      ],
    };
  },
};
</script>
