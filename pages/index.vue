<template>
  <section>
    <!-- <NavBar/> -->
    <Introduction/> 
    <History/>   
  </section>
</template>

<script>

// import NavBar from '~/components/NavBar';
import Introduction from '~/components/Introduction';
import History from '~/components/History';

export default {
    name: "Index",
    components: {
      // NavBar,
      Introduction,
      History
  }
}
</script>
