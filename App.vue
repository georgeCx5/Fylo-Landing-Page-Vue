<script>
import logo from '@/assets/images/logo.svg?url'
import imgHeader from '@/assets/images/illustration-1.svg?url'

export default {
  data() {
    return {
      logo,
      imgHeader,
    }
  },
  components: {
  }
}
</script>
<template>
  <header class=" mx-6 mt-6">
    <nav class=" flex justify-between items-center">
      <img class=" w-20" :src="logo" alt="logo">
      <div class=" flex justify-between w-[167px] text-[12px] leading-[14px]">
        <h3>Features</h3>
        <h3>Team</h3>
        <h3>Sign In</h3>
      </div>
    </nav>
    <div>
      <img :src="imgHeader" alt="imgHeader">
      <h1 class=" text-[24px] leading-[36px]">All your files in one secure location, accessible anywhere.</h1>
      <p class=" text-[14px] leading-[21px]">
        Fylo stores your most important files in one secure location.
        Access them wherever you need, share and collaborate with friends,
        family, and co-workers.
      </p>
      <input class=" border border-black w-full" type="email">
      <button type="submit"></button>
    </div>
  </header>
</template>