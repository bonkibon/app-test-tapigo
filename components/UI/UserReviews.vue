<template>
    <div class="container">
        <form>
            <div class="form-group">
                <label for="commentText">Comment</label>
                <textarea class="form-control" id="commentText" rows="3"></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
        </form>
    </div>
    <div class="container">
        <h3>Отзывы</h3>
        <div class="container_offset">
            <ul>
                <li v-for="review in item" :key="review.id">
                    <h5>{{ review.author }}</h5>
                    <p>{{ review.text }}</p>
                    
                    <div class="container_upvote">
                        <button type="button" class="btn btn-primary btn-sm">Ответить</button>
                    </div>
                    
                    <ul v-if="review.replies && review.replies.length">
                        <li v-for="reply in review.replies" :key="reply.id">
                            <h6>{{ reply.author }}</h6>
                            <p>{{ reply.text }}</p>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        item: [],
    }
};
</script>

<style scoped>
.container_offset {
    margin: 0 auto;
    margin-left: 0px;
}

.container_upvote {
    margin-bottom: 15px;
}
</style>    