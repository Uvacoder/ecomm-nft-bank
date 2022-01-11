<template>
  <article>
    <header> 
        <p>
          <span class="published">Published:</span>
          <span>{{ article.published }}</span>
        </p> 
        <ul class="tags"> 
          <li v-for="tag in article.tags" :key="tag" class="tag">
            <nuxt-link
              :to="{ name: 'tags-tag', params: { tag: tag.toLowerCase() } }"
              class="hover:underline"
            >
              {{ tag }}
            </nuxt-link>
          </li>
        </ul>  
    </header>
    <main class="content">
      <nuxt-content :document="article" />
    </main> 
    <div class="blog-prev">
      <prev-next :prev="prev" :next="next" /> 
    </div>
  </article>
</template>
<style scoped>
 article {
   margin: 0;
   padding: 0;
   width: 100vw;
   height: 100%;
   min-height: 100vh;
   font-family: "Titillium Web", sans-serif;
 }

 .content, header,.blog-prev {
   width: 60%;
   margin: auto;
 }

 header p {
   font-size: 2.3em;
 }

 header .published {
   font-style: italic;
 }

 .blog-prev * {
   display: flex;
   gap: 3em;
 }

 .blog-prev a {
   background: blanchedalmond;
 }

 .tags {
   display: flex; 
   padding: 0;
   text-align: right;
   gap: 1em;  
 }

 .tags .tag {
   background: #C33764;  /* fallback for old browsers */
   background: -webkit-linear-gradient(to right, #1D2671, #C33764);  /* Chrome 10-25, Safari 5.1-6 */
   background: linear-gradient(to right, #1D2671, #C33764); 
   color: wheat;
   padding: 0.4em;
   border-radius: 0.3em;
   text-align: left;
 }
</style>
<script>
import global from '@/utils/global';
import getSiteMeta from '@/utils/getSiteMeta'; 

export default {
  name: 'ArticlePage',
  layout: 'PageLayout',
  async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch();

    const [prev, next] = await $content('articles')
      .only(['title', 'slug', 'published'])
      .sortBy('published', 'desc')
      .surround(params.slug)
      .fetch();

    return {
      article,
      prev,
      next,
    };
  },
  computed: {
    meta() {
      const metaData = {
        type: 'article',
        title: this.article.title,
        description: this.article.description,
        url: `${this.$config.baseUrl}/articles/${this.$route.params.slug}`,
        mainImage: this.article.image,
      };
      return getSiteMeta(metaData);
    },
  },
  head() {
    return {
      title: this.article.title,
      meta: [
        ...this.meta,
        {
          property: 'article:published_time',
          content: this.article.createdAt,
        },
        {
          property: 'article:modified_time',
          content: this.article.updatedAt,
        },
        {
          property: 'article:tag',
          content: this.article.tags ? this.article.tags.toString() : '',
        },
        { name: 'twitter:label1', content: 'Written by' },
        { name: 'twitter:data1', content: global.author || '' },
        { name: 'twitter:label2', content: 'Filed under' },
        {
          name: 'twitter:data2',
          content: this.article.tags ? this.article.tags.toString() : '',
        },
      ],
      link: [
        {
          hid: 'canonical',
          rel: 'canonical',
          href: `${this.$config.baseUrl}/articles/${this.$route.params.slug}`,
        },
      ],
    };
  },
};
</script>
