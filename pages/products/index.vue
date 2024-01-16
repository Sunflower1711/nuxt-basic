<template>
    <div class="container">
        <div v-for="product in data.products">
            <NuxtLink :to="`/products/${product.id}`">
                <h2 class="title">{{ product.title }}</h2>
                <img :src=product.thumbnail>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
useHead({
    title: "All Product",
    meta: [{
        name: "description",
        content: "Product of True",
    }]
})

const { data: data } = await useFetch('https://dummyjson.com/products?limit=10')
console.log(data);
</script>

<style  scoped>
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.container div {
    width: 300px;
    height: 300px;
    margin: 30px 15px;
    background-color: #333;
}

.container div:hover {
    background-color: orange;
}

.title {
    color: white;
    text-align: center;
    font-size: 1.2rem;
}

img {
    width: 300px;
    height: 300px;
    object-fit: cover;
}

a {
    text-decoration: none;
}
</style>