<template>
    <div class="admin-new-post-page">
        <section class="new-post-form">
            <AdminPostForm />
        </section>
    </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'
export default {
    layout: 'admin',
    components: {
        AdminPostForm,
    }
}
</script>
<style scoped>
.admin-new-post-page {
    width: 60%;
    margin: auto;
}
</style>