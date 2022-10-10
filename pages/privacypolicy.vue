<template>
  <section>
    <BackTop/>
    <CustomNavbar/>
    <Privacy/>
    <Footer/>
  </section>
</template>

<script>

import BackTop from '~/components/BackTop';
import CustomNavbar from '~/components/CustomNavbar';
import Privacy from '~/components/Privacy';
import Footer from "~/components/Footer";

export default {
    name: "Index",              
    components: {
      BackTop,
      CustomNavbar,
      Privacy,
      Footer
  }
}
</script>