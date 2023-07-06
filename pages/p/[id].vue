<template>
    <div>
        <h1>Viewing paste {{ id }}</h1>
        <h2>{{ data.data.title }}</h2>
        <p>{{ data.data.body }}</p>
    </div>
</template>

<script setup>
// grab the post id from the url
const { id } = useRoute().params
const api_url = 'https://szsaextmvibiosujacix.supabase.co/functions/v1/get_paste_by_uuid';
const { data: data, pending, error, refresh } = await useFetch(api_url, {
    key: id,
    method: 'POST',
    body: {
        uuid: id
    }
})
</script>

<style scoped></style>
