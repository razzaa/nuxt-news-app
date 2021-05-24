<template>
    <div class="admin-post-page">
        <section class="update-form">
            <AdminPostForm :post="loadedPost" />
        </section>
    </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'
export default {
    layout: 'admin',
    components: {
        AdminPostForm
    },
    data() {
        return {
            loadedPost: {
                author: 'Ali',
                title: 'My Awesome Post',
                content: 'Super amazing, thanks for that!',
                thumbnailLink: 'https://images.pexels.com/photos/546819/pexels-photo-546819.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
            }
        }
    }
}
</script>
<style scoped>
.admin-post-page {
    width: 60%;
    margin: auto;
}
</style>