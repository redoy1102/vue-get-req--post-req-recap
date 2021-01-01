<template>
  <div class="container">
    <compNavbar></compNavbar>
    <compPeoples></compPeoples>
    <compBlog></compBlog>
    <compNams></compNams>
    <compEmls></compEmls>
    <compPhnnmbrs></compPhnnmbrs>

  </div>
</template>

<script>
import compNavbar from './Components/Navbar'
import compBlog from './Components/Blog'
import compPeoples from './Components/Peoples'
import compNams from './Components/nams'
import compEmls from './Components/emls'
import compPhnnmbrs from './Components/phnnmbrs'

export default {
  components: {
    compNavbar,
    compBlog,
    compPeoples,
    compNams,
    compEmls,
    compPhnnmbrs,
  }
}
</script>