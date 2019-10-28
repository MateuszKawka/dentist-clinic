<template>
  <section class="section blog" id="blog">
    <h2 class="section__title">Blog</h2>
    <BlogItem />
    <BlogItem />
    <BlogItem />
    <button class="button" type="button">Check out our blog</button>
  </section>
</template>

<script>
import BlogItem from '@/components/BlogItem'

export default {
  name: 'Blog',
  components: {
    BlogItem
  }
}
</script>