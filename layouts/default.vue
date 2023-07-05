<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <h1>🍝 pastes.ayrscott.com</h1>
                <ul>
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
        <div>
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

h1 {
    font-size: 40px;

}
</style>
