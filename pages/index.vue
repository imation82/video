<template>
  <section>
    <!-- <NavBar/> -->
    <Introduction/> 
    <History/>
    <Connect/>   
  </section>
</template>

<script>

// import NavBar from '~/components/NavBar';
import Introduction from '~/components/Introduction';
import History from '~/components/History';
import Connect from '~/components/Connect';

export default {
    name: "Index",
    components: {
      // NavBar,
      Introduction,
      History,
      Connect
  }
}
</script>
