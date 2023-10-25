<template>
  <div v-for="item in data_post" :key="item.title">
    <BasePost :item="item" @click="subbmitted(item.id)" />
  </div>
</template>

<script>

import BasePost from "@/components/UI/BasePost.vue";

export default {
  methods: {
    subbmitted(id) {
      this.$router.push(`/base_post/${id}`)
    }
  },
  components: {
    BasePost,
  },
  // TODO: Использование централизованного хранения + api запросы
  data() {
    return {
      data_post: [
        {
          id: 0,
          img: "https://i.artfile.ru/2000x1333_1569238_[www.ArtFile.ru].jpg",
          title: "Заголовок поста",
          description: "Мини-описание",
        },
        {
          id: 1,
          img: "https://i.pinimg.com/originals/3a/8b/3d/3a8b3ddb20ba68f13a58e7b68c2b5220.jpg",
          title: "Заголовок поста",
          description: "Мини-описание",
        },
      ]
    }
  },
};
</script>