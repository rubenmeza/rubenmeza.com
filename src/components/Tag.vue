<template>
  <span class="tag">
    <slot></slot>
  </span>
</template>

<script>
export default {

}
</script>

<style>
.tag {
  @apply text-xs py-1 px-1 bg-gray-300 text-gray-500 rounded-sm;
}
</style>
