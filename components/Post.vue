<template>
    <div class="post">
        <h1 class="post__title">
            <nuxt-link :to="{ name: 'posts-id', params: { id: post.id } }">{{ post.title }}</nuxt-link>
            <!-- to get the name, simply look for the 'name' router.js in .nuxt folder -->
        </h1>

        <p>{{ post.body }}</p>
    </div>
</template>

<script>
    export default {
    	props: {
    		post: Object
        }
    }
</script>

<style lang="scss">
    .post {
        margin-bottom: 40px;

        &__title {
            font-size: 3em;
        }
    }
</style>

