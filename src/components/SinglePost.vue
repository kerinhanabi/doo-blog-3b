<template>
    <div class="post">
        <h3>{{ post.title }}</h3>
        <!-- p>{{ post.body }}</p -->
         <!-- to use snippet here via setup the return from setup -->
          <p>{{ snippet }}</p>
    </div>
</template>

<script>
import { computed } from 'vue'

export default {
    props: ['post'],
    setup(props) {
        const snippet = computed(() => {
            return props.post.body.substring(0,100) + '....'
        })

        return { snippet }
    }
}
</script>

<style>

</style>