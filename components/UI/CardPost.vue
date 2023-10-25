<template>
    <div class="container">
        <div class="container_offset">
            <h1>{{ item.title }}</h1>
        </div>
    </div>

    <div class="container">
        <div class="container_offset">
            <h4>{{ item.description }}</h4>
        </div>
    </div>

    <div class="container">
        <img v-bind:src="item.img" class="card-img-top">
    </div>

    <div class="container">
        <div class="container_offset">
            <h5>{{ item.published_date }}</h5>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardPost",
    data() {
        return {}
    },
    mounted() {
    },
    props: {
        item: {
            img: {
                type: String,
                default: '',
            },
            title: {
                type: String,
                default: '',
            },
            description: {
                type: String,
                default: '',
            },
            published_date: {
                type: String,
                default: '',
            },
            subbmitted: {
                type: Function,
                defaut: () => {

                }
            }
        },
    }
}
</script>


<style scoped>
.container_offset {
    margin: 0 auto;
    margin-left: 0px;
}
</style>