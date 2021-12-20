<template>
  <v-app>
    <Appbar />
    <v-main>
      <!-- Paralax Component -->
      <Beranda id="beranda"/>
      <!-- Hero Component -->
      <Selayangpandang id="selayang-pandang"/>
      <!-- Gallery Component -->
      <Gallery id="gallery" />
      <!-- Project Component -->
      <Project id="project"/>
      <!-- Aboutus Component -->
      <Aboutus id="about-us" />
      <!-- Contact Component -->
      <Contact id="contact"/>
      <!-- Footer Component -->
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Appbar from './components/app/Appbar.vue'
import Selayangpandang from './components/app/Selayangpandang.vue'
import Beranda from './components/app/Beranda.vue'
import Aboutus from './components/app/Aboutus.vue'
import Gallery from './components/app/Gallery.vue'
import Project from './components/app/Project.vue'
// import hmmm from './components/app/hmmm.vue'
import Contact from './components/app/Contact.vue'
import Footer from './components/app/Footer.vue'

export default {
  name: 'App',

  components: {
    Appbar,
    Beranda,
    Selayangpandang,
    Gallery,
    Aboutus,
    Project,
    Contact,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
