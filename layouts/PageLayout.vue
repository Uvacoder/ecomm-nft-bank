<template>
  <div>
    <PageHeader/>
    <main>
      <div>
        <Nuxt />
      </div>
    </main>
    <Footer />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader';
import Footer from '@/components/Footer';

export default {
  name: 'PageLayout',
  components: {
    PageHeader,
    Footer,
  },
};
</script>
