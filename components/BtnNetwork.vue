<script>
export default {
   data() {
      return {
         isHover: false,
      }
   },
   props: {
      netName: String,
   },
   computed: {
      hoverState() {
         return this.isHover ? 'fill-neo-hover-blue' : 'fill-white';
      }
   }
}
</script>
<template>
   <!-- <h5>{{ isHover }}</h5> -->
   <button
      class=" flex justify-center items-center w-7 dsk:w-8 h-7 dsk:h-8 p-[6px] border border-white hover:border-neo-hover-blue rounded-full"
      @mouseover="isHover = true" @mouseout="isHover = false">
      <!-- Networks -->
      <svg v-if="netName == 'facebook'" viewBox="0 0 56.693 56.693" xml:space="preserve"
         xmlns="http://www.w3.org/2000/svg">
         <path
            d="M40.43 21.739h-7.645v-5.014c0-1.883 1.248-2.322 2.127-2.322h5.395V6.125l-7.43-.029c-8.248 0-10.125 6.174-10.125 10.125v5.518h-4.77v8.53h4.77v24.137h10.033V30.269h6.77l.875-8.53z"
            :class="`${hoverState}`">
         </path>
      </svg>
      <svg v-if="netName == 'twitter'" viewBox="0 0 56.693 56.693" xml:space="preserve" xmlns="http://www.w3.org/2000/svg">
         <path
            d="M52.837 15.065a20.11 20.11 0 0 1-5.805 1.591 10.125 10.125 0 0 0 4.444-5.592 20.232 20.232 0 0 1-6.418 2.454 10.093 10.093 0 0 0-7.377-3.192c-5.581 0-10.106 4.525-10.106 10.107 0 .791.089 1.562.262 2.303-8.4-.422-15.848-4.445-20.833-10.56a10.055 10.055 0 0 0-1.368 5.082c0 3.506 1.784 6.6 4.496 8.412a10.078 10.078 0 0 1-4.578-1.265l-.001.128c0 4.896 3.484 8.98 8.108 9.91a10.162 10.162 0 0 1-4.565.172c1.287 4.015 5.019 6.938 9.441 7.019a20.276 20.276 0 0 1-12.552 4.327c-.815 0-1.62-.048-2.411-.142a28.6 28.6 0 0 0 15.493 4.541c18.591 0 28.756-15.4 28.756-28.756 0-.438-.009-.875-.028-1.309a20.47 20.47 0 0 0 5.042-5.23z"
            :class="`${hoverState}`"></path>
      </svg>
      <svg v-if="netName == 'instagram'" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 56.7 56.7" xml:space="preserve">
         <path
            d="M28.2 16.7c-7 0-12.8 5.7-12.8 12.8s5.7 12.8 12.8 12.8S41 36.5 41 29.5s-5.8-12.8-12.8-12.8zm0 21c-4.5 0-8.2-3.7-8.2-8.2s3.7-8.2 8.2-8.2 8.2 3.7 8.2 8.2-3.7 8.2-8.2 8.2z"
            :class="`${hoverState}`"></path>
         <circle cx="41.5" cy="16.4" r="2.9" :class="`${hoverState}`"></circle>
         <path
            d="M49 8.9c-2.6-2.7-6.3-4.1-10.5-4.1H17.9c-8.7 0-14.5 5.8-14.5 14.5v20.5c0 4.3 1.4 8 4.2 10.7 2.7 2.6 6.3 3.9 10.4 3.9h20.4c4.3 0 7.9-1.4 10.5-3.9 2.7-2.6 4.1-6.3 4.1-10.6V19.3c0-4.2-1.4-7.8-4-10.4zm-.4 31c0 3.1-1.1 5.6-2.9 7.3s-4.3 2.6-7.3 2.6H18c-3 0-5.5-.9-7.3-2.6C8.9 45.4 8 42.9 8 39.8V19.3c0-3 .9-5.5 2.7-7.3 1.7-1.7 4.3-2.6 7.3-2.6h20.6c3 0 5.5.9 7.3 2.7 1.7 1.8 2.7 4.3 2.7 7.2v20.6z"
            :class="`${hoverState}`"></path>
      </svg>
   </button>
</template>