<template>
    <div>
        <h1 class="text-4xl pb-4 font-bold text-center">Greetings</h1>
        <p class="pb-4">Welcome to pastes.ayrscott.com, a simple place to share the latest and greatest in all things copy
            pasta 🍝</p>
        <form action="/api/new" method="POST">
            <h2 class="text-2xl font-bold pb-2">Post Title (optional)</h2>
            <input type="text" name="title" placeholder="Title"
                class="block p-2.5 w-full  text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500" /><br />
            <h2 class="text-2xl font-bold pb-2">Paste Text</h2>
            <textarea id="content" rows="4"
                class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500"
                placeholder="Paste your text here..."></textarea>
            <input class="btn mx-auto block mt-8" type="submit" value="Paste It!" />
        </form>
    </div>
</template>

<script setup>

</script>

<style scoped></style>