
<template>
    <div class="container">

        <div class="form-group">
            <input type="text" class="form-control" placeholder="Заголовок поста">
        </div>
        <div class="form-group">
            <input type="text" class="form-control" placeholder="Картинка для поста">
        </div>
        <div class="form-group">
            <input type="text" class="form-control" placeholder="Описание для поста">
        </div>
        <button type="button" class="btn btn-success" @click.prevent="submitted">Добавить</button>
    </div>
</template>

<script>

export default {
    name: "PostInput",
    props: {
        subbmitted: {
            type: Function,
            defaut: () => {

            }
        }
    },
}

</script>