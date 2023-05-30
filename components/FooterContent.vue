<script>
export default {
   props: {
      content: String,
   }
}
</script>
<template>
   <h5>
      <button class=" hover:text-neo-hover-blue">{{ content }}</button>
   </h5>
</template>