<template>
    <div>

        <Head>
            <Title>Pastes</Title>
        </Head>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <div class="font-bold">
                    <!-- ignore router link active -->
                    <NuxtLink to="/">🍝 pastes.ayrscott.com</NuxtLink>
                </div>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/p/721adcd8-64b7-4b0b-89e0-4ba563d57bb4">View Paste</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.router-link-active {
    font-weight: bold;
    color: green;
}
</style>
