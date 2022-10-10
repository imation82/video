<template>
  <section>
    <BackTop/>
    <CustomNavbar/>
    <Terms/>
    <Footer/>
  </section>
</template>

<script>

import BackTop from '~/components/BackTop';
import CustomNavbar from '~/components/CustomNavbar';
import Terms from '~/components/Terms';
import Footer from "~/components/Footer";

export default {
    name: "Index",              
    components: {
      BackTop,
      CustomNavbar,
      Terms,
      Footer
  }
}
</script>