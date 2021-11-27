<template>
  <div>
    <Navbar/>
    <CoverLetter/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import CoverLetter from '@/components/CoverLetter.vue'

export default {
  name: 'Home',
  components: {
    Navbar,
    CoverLetter
  }
}
</script>