<template>
    <div class="container">
        <h1>เกี่ยวกับผู้พัฒนาเว็บไซต์</h1>
        <img src="/image/fish.jpg">
    </div>
</template>

<script setup>
useHead({
    title: "About",
    meta: [{
        name: "description", content: "about Dev"
    }]
})
</script>

<style  scoped>
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