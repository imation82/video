<template>
  <section>
    <BackTop/>
    <NavBar/>
    <Introduction/> 
    <History/>
    <Connect/>
    <Discover/>   
    <Download/>
    <Testimonial/>
    <Team/>
    <Footer/>
  </section>
</template>

<script>

import BackTop from '~/components/BackTop';
import NavBar from '~/components/NavBar';
import Introduction from '~/components/Introduction';
import History from '~/components/History';
import Connect from '~/components/Connect';
import Discover from '~/components/Discover';
import Download from '~/components/Download';
import Testimonial from '~/components/Testimonial';
import Team from '~/components/Team';
import Footer from "~/components/Footer";

export default {
    name: "Index",
    components: {
      BackTop,
      NavBar,
      Introduction,
      History,
      Connect,
      Discover,
      Download,
      Testimonial,
      Team,
      Footer
  }
}
</script>
