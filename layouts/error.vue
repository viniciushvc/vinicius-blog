<template>
  <Container>
    <h1 v-if="error.statusCode === 404">
      Page not found
    </h1>
    <h1 v-else>
      An error occurred
    </h1>
    <n-link to="/">
      Home page
    </n-link>
  </Container>
</template>

<script>
export default {
  components: {
    Container: () => import('@/components/Container'),
  },
  props: {
    error: {
      type: Object,
      required: true,
    },
  },
}
</script>
