<template>
  <div>
    <button @click="emitclicked()" class="py-2 px-5 text-white focus:text-white hover:text-white bg-primary hover:bg-secondary focus:bg-secondary font-medium text-base 2xl:text-lg justify-center duration-300 ease-in-out rounded-md outline-none focus:outline-none" :class="flexdisplay ? 'flex w-full' : 'block w-fit'">
      <slot />
    </button>
  </div>
</template>

<script>
export default {
  props: {
    flexdisplay: Boolean
  },
  methods: {
    emitclicked(){
      this.$emit("clicked")
    }
  }
}
</script>

<style>

</style>