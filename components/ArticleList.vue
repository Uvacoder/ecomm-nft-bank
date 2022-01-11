<template>
<ul class="articles">
  <li  v-for="article of articles"
        :key="article.slug">
        <div class="card-link">
        <article class="blog-card">
          <img class="post-image" v-if="article.image"
            :src="article.image" alt="vitateach" />
          <div class="article-details">
            <h4 class="post-category"><span>{{article.tags[0]}}</span></h4>
            <h3 class="post-title">{{ article.title }}</h3>
            <p class="post-description">{{ article.description }}
            <NuxtLink :to="{ name: 'articles-slug', params: { slug: article.slug } }"> 
            <br/>Read More <span>&hellip;</span></NuxtLink>
            </p>
            <p class="post-author">By {{ article.author }}</p>
          </div>
        </article>
      </div> 
  </li>
  <!-- <div v-if="total" class="constainer mx-auto my-5 max-w-5xl">
  <Pagination v-if="total > 5" :total="total" />
</div>  -->
</ul>   
</template>
<script>
import Pagination from '@/components/Pagination'; 
export default {
  name: 'ArticleList',
  components: {
    Pagination,
  },
  props: {
    articles: {
      type: Array,
      default: Array,
    },
    total: {
      type: Number,
      default: 0,
    },
  },
};
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:400,700');
 .articles {
   width: 100vw;  
   background-color: snow;
   margin: 0;
   padding: 0; 
   overflow: hidden;
   font-family: "Titillium Web", sans-serif;
 }

 .articles li {
   margin: 1em;
 }
 .blog-card {
	 display: flex;
	 flex-direction: row;
	 background: #fff;
	 box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
   width: 55vw;
	 border-radius: 0.375rem; 
   margin: auto;
	 overflow: hidden; 
}
 .card-link {
	 position: relative;
	 display: block;
	 color: inherit;
	 text-decoration: none;
}
 .card-link:hover .post-title, .post-category {
	 transition: color 0.3s ease;
	 color: #e04f62;
}
 .card-link:hover .post-image, .post-category {
	 transition: opacity 0.3s ease;
	 opacity: 0.9;
}
 .post-image {
	 transition: opacity 0.3s ease;
	 display: block;
	 width: 100%;
	 object-fit: cover;
}
 .article-details {
	 padding: 1.5rem;
}
 .post-category {
	 display: inline-block;
	 text-transform: uppercase;
	 font-size: 0.75rem;
	 font-weight: 700;
	 line-height: 1;
	 letter-spacing: 0.0625rem;
	 margin: 0 0 0.75rem 0;
	 padding: 0 0 0.25rem 0;
	 border-bottom: 0.125rem solid #ebebeb;
}
 .post-title {
	 transition: color 0.3s ease;
	 font-size: 1.125rem;
	 line-height: 1.4;
	 color: #121212;
	 font-weight: 700;
	 margin: 0 0 0.5rem 0;
}
 .post-author {
	 font-size: 0.875rem;
	 line-height: 1;
	 margin: 1.125rem 0 0 0;
	 padding: 1.125rem 0 0 0;
	 border-top: 0.0625rem solid #ebebeb;
}
 @media (max-width: 40rem) {
	 #container {
		 width: 18rem;
		 height: 27.25rem;
	}
	 .blog-card {
		 flex-wrap: wrap;
	}
}
 @supports (display: grid) {
	 body {
		 display: grid;
		 grid-template-columns: repeat(4, 1fr);
		 grid-gap: 0.625rem;
		 grid-template-areas: ". main main ." ". main main ."; 
	}
	 #container {
		 grid-area: main;
		 align-self: center;
		 justify-self: center;
	}
	 .post-image {
		 height: 100%;
	}
	 .blog-card {
		 display: grid;
		 grid-template-columns: 1fr 2fr;
		 grid-template-rows: 1fr;
	}
	 @media (max-width: 40rem) {
		 .blog-card {
			 grid-template-columns: auto;
			 grid-template-rows: 12rem 1fr;
		}
	}
}
 
</style>
