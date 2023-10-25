<template>
  <NuxtLayout>
    <NuxtPage/>
  </NuxtLayout>

  <div class="container">
    <button @click.prevent="openPostsPage()">Открыть страницу с постами</button>
  </div>
</template>

<script>

export default {
  methods: {
    openPostsPage() {
      this.$router.push('base_post')
    }
  }
};
</script>
