<template>
    <div class="container">
        <h1>First Page</h1>
        <img src="/image/profile.jpg">
    </div>
</template>

<script setup>
useHead({
    title: "Main",
    meta: [{
        name: "description", content: "Frist"
    }]
})
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

img {

    width: 400px;
    height: auto;
    object-fit: cover;
}
</style>