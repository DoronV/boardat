<template>
    <div>
        <h1>Restaurants</h1>
        <div v-for="item in items" :key="item.id">
            <h2>{{ item.attributes.Name }}</h2>
            <p>{{ item.attributes.Description }}</p>
            <img :src="'http://localhost:1337' + item.attributes.image.data.attributes.formats.thumbnail.url" alt="Image">
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            items: [],
        };
    },
    async created() {
        const response = await axios.get('http://localhost:1337/api/restaurants?populate=image');
        console.log(response.data.data[1].attributes.image.data.attributes.url);
        this.items = response.data.data;
    },
};
</script>