<template>
    <div class="single-post-page">
        <section class="post">
            <h1 class="post-title">{{loadedPost.title}}</h1>
            <div class="post-details">
                <div>Last updated on {{loadedPost.updatedDate}}</div>
                <div>Written by {{loadedPost.author}}</div>
            </div>
            <p class="post-content">{{loadedPost.content}}</p>
        </section>
        <section class="post-feedback">
            <p>Let me know what you think about the post, send a mail to <a href="mailto:ali@test.com">ali@test.com</a></p>
        </section>
    </div>
</template>

<script>
export default {
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPost: {
          id: '3',
          title: 'First Post (ID: ' + context.route.params.id + ')',
          previewText: 'Super amazing, thanks for that!',
          author: 'Ali Raza',
          updatedDate: new Date,
          content: 'Some dumy text which is definitely not the preview text though!',
          thumbnail: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
        }
      })
    },1000);
  }
}
</script>

<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}

.post {
  width: 100%;
}

@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}

.post-title {
  margin: 0;
}

.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}

.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}

.post-feedback a {
  color: red;
  text-decoration: none;
}

.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
</style>