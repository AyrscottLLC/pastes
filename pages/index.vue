<template>
    <div>
        <h1 class="text-4xl pb-4 font-bold text-center">Greetings</h1>
        <p class="pb-4">Welcome to pastes.ayrscott.com, a simple place to share the latest and greatest in all things copy
            pasta 🍝</p>
        <form action="/api/new" method="POST">
            <h2 class="text-2xl font-bold pb-2">Post Title (optional)</h2>
            <input id="title" type="text" name="title" placeholder="Title"
                class="block p-2.5 w-full  text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500" /><br />
            <h2 class="text-2xl font-bold pb-2">Paste Text</h2>
            <textarea id="content" rows="8"
                class="font-mono block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500"
                placeholder="Paste your text here..."></textarea>
            <input id="pasteit" class="btn mx-auto block mt-8" type="submit" value="Paste It!"
                @click.prevent="submitForm" />
        </form>
    </div>
</template>

<script setup>
// submitForm needs to be handled down here
const submitForm = () => {

    // disable the button to prevent double submission
    document.querySelector('#pasteit').disabled = true

    // grab the title from the input
    const title = document.getElementById('title').value

    // grab the content from the textarea
    const content = document.getElementById('content').value

    // post the content to the api
    fetch('https://szsaextmvibiosujacix.supabase.co/functions/v1/paste', {
        method: 'POST',
        body: JSON.stringify({
            title: title,
            body: content
        })
    })
        // redirect to the new paste
        .then(res => res.json())
        .then(data => {
            // console.log(data)
            window.location.href = `/p/${data[0].uuid}`
        }).catch(err => {

            // disable the button to prevent double submission
            document.querySelector('#pasteit').disabled = false

            console.error(err)
        })
}

</script>

<style scoped></style>