<template>
    <div>
        <h1 class="text-4xl pb-4 font-bold">Greetings</h1>
        <p class="pb-4">Welcome to pastes.ayrscott.com, a simple place to share the latest and greatest in all things copy
            pasta 🍝</p>
        <form action="/api/new" method="POST">
            <h2 class="text-2xl font-bold pb-2">Post Title (optional)</h2>
            <input type="text" name="title" placeholder="Title" /><br />
            <h2 class="text-2xl font-bold pb-2">Paste Text</h2>
            <textarea name="content" placeholder="Content"></textarea><br />
            <input class="btn" type="submit" value="Paste It!" />
        </form>
    </div>
</template>

<script setup>

</script>

<style scoped></style>