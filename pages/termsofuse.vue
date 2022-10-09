<template>
  <section>
    <CustomNavbar/>
    <Terms/>
    <Footer/>
  </section>
</template>

<script>

import CustomNavbar from '~/components/CustomNavbar';
import Terms from '~/components/Terms';
import Footer from "~/components/Footer";

export default {
    name: "Index",              
    components: {
      CustomNavbar,
      Terms,
      Footer
  }
}
</script>