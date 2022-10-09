<template>
  <section>
    <CustomNavbar/>
    <Privacy/>
    <Footer/>
  </section>
</template>

<script>

import CustomNavbar from '~/components/CustomNavbar';
import Privacy from '~/components/Privacy';
import Footer from "~/components/Footer";

export default {
    name: "Index",              
    components: {
      CustomNavbar,
      Privacy,
      Footer
  }
}
</script>