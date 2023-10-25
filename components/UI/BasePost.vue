<template>
    <div class="container">
        <div class="card">

            <div v-if="item.img.length > 0">
                <img v-bind:src="item.img" class="card-img-top">
            </div>
            <div v-else>
                <img src="../../static/error.jpeg" class="img-fluid" alt="...">
            </div>

            <div class="card-body">
                <h5 class="card-title">{{ item.title }}</h5>
                <p class="card-text">{{ item.description }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BasePost",
    data() {
        return {}
    },
    mounted() {
    },
    props: {
        item: {
            id: {
                type: Number,
                default: 0,
            },
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
        },
    }
}
</script>


<style scoped>
.card {
    border: 2px solid rgba(0, 0, 0, 0.125);
}

.card-text {
    overflow: hidden;
    max-width: 75ch;
    white-space: nowrap;
}

img {
    max-width: 800px;
    max-height: 400px;
}
</style>