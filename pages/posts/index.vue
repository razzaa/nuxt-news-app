<template>
    <div class="post-list">
        <PostList :posts="loadedPosts"/>
    </div>
</template>

<script>
import PostList from '@/components/Posts/PostList'
export default {
  components: {
    PostList
  },  
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: '1',
              title: 'First Post',
              previewText: 'Super amazing, thanks for that!',
              thumbnail: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
            {
              id: '2',
              title: 'Second Post',
              previewText: 'Super amazing, thanks for that!',
              thumbnail: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
            {
              id: '3',
              title: 'Third Post',
              previewText: 'Super amazing, thanks for that!',
              thumbnail: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            },
          ]
        })
      },1000);
    })
    .then(data => {
      return data
    })
    .catch(e => {
      context.error(new Error())
    })
    
  },

}
</script>

<style scoped>
.posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>