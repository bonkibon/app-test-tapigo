<template>
    <CardPost :item="data_post[$route.params.id]" />
    <UserReviews :item="reviews" />
</template>

<script>

import CardPost from "@/components/UI/CardPost.vue";
import UserReviews from "@/components/UI/UserReviews.vue";

export default {
    // TODO: Использование централизованного хранения + api запросы
    data() {
        return {
            data_post: [
                {
                    id: 0,
                    img: "https://i.artfile.ru/2000x1333_1569238_[www.ArtFile.ru].jpg",
                    title: "Заголовок поста",
                    description: "Мини-описание",
                    published_date: '25.10.2023',
                },
                {
                    id: 1,
                    img: "https://i.pinimg.com/originals/3a/8b/3d/3a8b3ddb20ba68f13a58e7b68c2b5220.jpg",
                    title: "Заголовок поста",
                    description: "Мини-описание",
                    published_date: '25.10.2023',
                },
            ],
            reviews: [
                {
                    id: 1,
                    author: "Пользователь 1",
                    text: "Интересная картинка",
                    replies: [
                        {
                            id: 2,
                            author: "Пользователь 2",
                            text: "Спасибо за ваш отзыв!"
                        }
                    ]
                },
                {
                    id: 3,
                    author: "Пользователь 3",
                    text: "it`s amazing!!!"
                }
            ]
        }
    },
    components: {
        CardPost,
        UserReviews
    },
};
</script>