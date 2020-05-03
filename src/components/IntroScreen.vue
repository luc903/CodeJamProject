<template>
<h1>{{ greeting }}</h1>
</template>

<script>
export default {
  name: 'intro',
  props: {
    greeting: {
      type: String,
      required: true,
      default: 'Greetings!'
    }
  }
}
</script>
