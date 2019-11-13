<template>
  <div v-if="type === 'two'" class="Triangle Triangle--two" />
  <div v-else-if="type === 'one'" class="Triangle Triangle--one" />
  <div v-else-if="type === 'three'" class="Triangle Triangle--three" />
  <div v-else class="Triangle Triangle--four" />
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: ''
    }
  }
}
</script>
