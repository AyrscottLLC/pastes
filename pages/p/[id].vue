<template>
    <Head>
        <Title>{{ data.data.title }}</Title>
    </Head>
    <div>
        <em>paste {{ id }}</em>
        <h2 class="py-4 text-4xl font-bold">{{ data.data.title }}</h2>
        <pre>{{ data.data.body }}</pre>
    </div>
</template>

<script setup>

// grab the post id from the url
const { id } = useRoute().params

const { data, pending, error, refresh } = await useFetch('https://szsaextmvibiosujacix.supabase.co/functions/v1/get_paste_by_uuid', {
    key: id,
    method: 'POST',
    body: {
        uuid: id
    }
})

</script>

<style scoped></style>
