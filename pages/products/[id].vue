<template>
    <div>

        <head>
            <Title>Mini : {{ product.title }}</Title>
            <Meta name="desctiption" :content=product.description />
        </head>
        <div class="container">
            <img :src=product.thumbnail>
            <div class="detail">
                <h1>{{ product.title }}</h1>
                <h2>ราคา: ${{ product.price }}</h2>
                <h2>หมวดหมู่: {{ product.category }}</h2>
                <h3>แบรนด์: {{ product.brand }}</h3>
                <h4>ข้อมูลพื้นฐาน: {{ product.description }}</h4>
            </div>
        </div>
    </div>
</template>

<script setup>
const { id } = useRoute().params

const { data: product } = await useFetch('https://dummyjson.com/products/' + id)
</script>

<style  scoped>
.container {
    display: flex;
    justify-content: center;

}

.detail {
    padding-left: 10px;

}
</style>