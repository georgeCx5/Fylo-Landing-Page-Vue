<script>
import logo from '@/assets/images/logo.svg?url'
import imgHeader from '@/assets/images/illustration-1.svg?url'
import imgMain from '@/assets/images/illustration-2.svg?url'
import iconQuotes from '@/assets/images/icon-quotes.svg?url'
import iconArrow from '@/assets/images/icon-arrow.svg?component'
import imgAvatar from '@/assets/images/avatar-testimonial.jpg'


export default {
  data() {
    return {
      logo,
      imgHeader,
      imgMain,
      iconQuotes,
      imgAvatar,
    }
  },
  components: {
    iconArrow,
  }
}
</script>
<template>
  <header class=" flex flex-col gap-[98px] mx-6 dsk:mx-20 mt-6 dsk:mt-[65px]">
    <nav class=" flex justify-between items-center">
      <img class=" w-[80px] dsk:w-[166px]" :src="logo" alt="logo">
      <div
        class=" flex justify-between w-[167px] dsk:w-[271px] text-neo-dark-blue text-[12px] dsk:text-[16px] leading-[14px] dsk:leading-[19px] font-raleway font-medium">
        <h3>Features</h3>
        <h3>Team</h3>
        <h3>Sign In</h3>
      </div>
    </nav>
    <div class=" flex flex-col dsk:flex-row-reverse dsk:justify-end items-center gap-10 dsk:gap-[13px]">
      <img class=" w-[304px] dsk:w-[640px]" :src="imgHeader" alt="imgHeader">
      <div class=" flex flex-col gap-8 dsk:gap-[25px] dsk:w-[627px]">
        <div
          class=" flex flex-col items-center dsk:items-start gap-6 dsk:gap-[15px] text-center dsk:text-left text-neo-dark-blue font-open-sans">
          <h1 class=" w-[320px] dsk:w-[627px] text-[24px] dsk:text-[40px] leading-[36px] dsk:leading-[60px] font-bold">All
            your files in one secure location, accessible
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
  <main>
    <div class=" flex flex-col items-center px-7 bg-neo-grayish-blue">
      <img class=" w-[320px] dsk:w-[542px]" :src="imgMain" alt="imgMain">
      <div class=" w-[320px] dsk:w-[648px] text-center">
        <h2>Stay productive, wherever you are</h2>
        <div class=" dsk:w-[529px]">
          <p>
            Never let location be an issue when accessing your files. Fylo has you
            covered for all of your file storage needs.
          </p>
          <p>
            Securely share files and folders with friends, family and colleagues for
            live collaboration. No email attachments required!
          </p>
        </div>
      </div>

      <div class=" flex gap-2 items-center border-b border-neo-moderate-cyan">
        <button class=" text-neo-moderate-cyan">See how Fylo works</button>
        <iconArrow />
      </div>

      <div
        class=" flex flex-col justify-center gap-3 w-[280px] dsk:w-[356px] h-[170px] dsk:h-[215px] pl-[25px] pr-[12px] bg-white font-open-sans rounded shadow-xl">
        <img class=" w-[14px]" :src="iconQuotes" alt="iconQuotes">
        <p
          class=" text-[10px] dsk:text-[13px] leading-[18px] dsk:leading-[23px] tracking-[0.38px] dsk:tracking-[0.5px] font-medium">
          Fylo has improved our team productivity by an order of magnitude. Since
          making the switch our team has become a well-oiled collaboration machine.
        </p>
        <div class=" flex items-center gap-[7px]">
          <img class=" w-6 dsk:w-8 h-6 dsk:h-8 rounded-full" :src="imgAvatar" alt="imgAvatar">
          <div class=" flex flex-col gap-[2px]">
            <h5
              class=" text-[9px] dsk:text-[11px] leading-[12px] dsk:leading-[15px] tracking-[0.45px] dsk:tracking-[0.55px] font-bold">
              Kyle Burton</h5>
            <h6
              class=" text-[6px] dsk:text-[8px] leading-[12px] dsk:leading-[15px] tracking-[0.3px] dsk:tracking-[0.4px]">
              Founder & CEO, Huddle</h6>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
<style>
/* h6{
  font-size: xx-small;
} */
</style>