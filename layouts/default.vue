<template>
    <div>
        <h1>🍝 pastes.ayrscott.com</h1>
        <nav>
            <ul>
                <li>
                    <NuxtLink to="/">Home</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
            </ul>
        </nav>
        <slot />
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
