<template>
    <div>
        <h1>Greetings</h1>
        <p>Welcome to pastes.ayrscott.com, a simple place to share the latest and greatest in all things copy pasta 🍝</p>
        <form action="/api/new" method="POST">
            <input type="text" name="title" placeholder="Title" /><br />
            <textarea name="content" placeholder="Content"></textarea><br />
            <input type="submit" value="Submit" />
        </form>
    </div>
</template>

<script setup>

</script>

<style scoped></style>