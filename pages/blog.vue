<template>   
    <ArticleList :articles="paginatedArticles" :total="allArticles.length" />  
</template>

<script>
import getContent from '@/utils/getContent';
import ArticleList from '@/components/ArticleList'; 
import PageLayout from '@/layouts/PageLayout';

export default {
  name: 'HomePage',
  components: {
    ArticleList,
    PageLayout
  },
  async asyncData({ $content, app, params, error }) {
    const content = await getContent($content, params, error);
    return {
      allArticles: content.allArticles,
      paginatedArticles: content.paginatedArticles,
    };
  },
};
</script>