<template>
  <div>
    <Header />
    <main>
      <div>
        <Nuxt />
      </div>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header';
import Footer from '@/components/Footer';

export default {
  name: 'MainLayout',
  components: {
    Header,
    Footer,
  },
};
</script>
