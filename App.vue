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
}
</script>
<template>
  <header class=" flex flex-col gap-[98px] mx-6 dsk:mx-20 mt-6 dsk:mt-[65px]">
    <nav class=" flex justify-between items-center">
      <img class=" w-[80px] dsk:w-[166px]" :src="logo" alt="logo">
      <div class=" flex justify-between w-[167px] dsk:w-[271px] text-neo-dark-blue text-[12px] dsk:text-[16px] leading-[14px] dsk:leading-[19px] font-raleway font-medium">
        <h3>Features</h3>
        <h3>Team</h3>
        <h3>Sign In</h3>
      </div>
    </nav>
    <div class=" flex flex-col dsk:flex-row-reverse dsk:justify-end items-center gap-10 dsk:gap-[13px]">
      <img class=" w-[304px] dsk:w-[640px]" :src="imgHeader" alt="imgHeader">
      <div class=" flex flex-col gap-8 dsk:gap-[25px] dsk:w-[627px]">
        <div class=" flex flex-col items-center dsk:items-start gap-6 dsk:gap-[15px] text-center dsk:text-left text-neo-dark-blue font-open-sans">
          <h1 class=" w-[320px] dsk:w-[627px] text-[24px] dsk:text-[40px] leading-[36px] dsk:leading-[60px] font-bold">All your files in one secure location, accessible
            anywhere.</h1>
          <p class=" w-[296px] dsk:w-[585px] text-[14px] dsk:text-[17px] leading-[21px] dsk:leading-[24px] font-medium">
            Fylo stores your most important files in one secure location.
            Access them wherever you need, share and collaborate with friends,
            family, and co-workers.
          </p>
        </div>
        <div class=" flex flex-col dsk:flex-row gap-4 w-[304px] dsk:w-[536px] font-raleway">
          <input
            class=" border border-black dsk:w-[320px] h-10 px-5 placeholder:text-neo-light-gray text-[12px] leading-[14px] rounded-[3px]"
            type="email" placeholder="Enter your email">
          <button
            class=" dsk:w-[200px] h-10 bg-neo-bright-blue text-neo-grayish-blue text-[14px] leading-[16px] font-semibold rounded-[3px] shadow-lg"
            type="submit">Get Started</button>
        </div>
      </div>
    </div>
  </header>
</template>