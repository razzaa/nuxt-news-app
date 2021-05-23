<template>
    <section class="post-list">
      <PostPreview 
        id="1"
        :is-admin="isAdmin"
        thumbnail="https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
        title="Hello there!"
        previewText="This is my first post!"
        />
        <PostPreview 
        id="2"
        :is-admin="isAdmin"
        thumbnail="https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
        title="Hello there!"
        previewText="This is my 2nd post!"
        />
        <PostPreview 
        id="3"
        :is-admin="isAdmin"
        thumbnail="https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
        title="Hello there!"
        previewText="This is my third post!"
        />
        <PostPreview 
        id="4"
        :is-admin="isAdmin"
        thumbnail="https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
        title="Hello there!"
        previewText="This is my 4rth post!"
        />
    </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'
export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>