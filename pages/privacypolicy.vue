<template>
  <section>
    <Privacy/>
    <Footer/>
  </section>
</template>

<script>

import Privacy from '~/components/Privacy';
import Footer from "~/components/Footer";

export default {
    name: "Index",              
    components: {
      Privacy,
      Footer
  }
}
</script>