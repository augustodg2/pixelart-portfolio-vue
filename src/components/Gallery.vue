<template>
<section class="gallery">
    <ul>
        <li v-for="image in images" :key="image.src">
            <Image
                :size="image.size"
                :src="image.src"
                :alt="image.title"
            />
        </li>
    </ul>
</section>
</template>

<script>
import Image from './Image.vue';

export default {
    name: 'Gallery',
    props: {
        images: Object
    },
    components: {
        Image
    }
}
</script>

<style scoped>
.gallery ul {
    display: flex;
    margin: 0;
    padding: 0;
    margin-left: -20px;
    margin-bottom: -20px;
    flex-wrap: wrap;
    justify-content: center;
}

li {
    list-style: none;
    width: fit-content;
    margin-left: 20px;
    margin-bottom: 20px;
    display: flex;
}

@media screen and (max-width: 700px) {
    .gallery ul {
        margin-left: -5px;
        margin-bottom: -5px;
    }

    li {
        margin-left: 5px;
        margin-bottom: 5px;
    }
}
</style>