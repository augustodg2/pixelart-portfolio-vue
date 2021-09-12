<template>
    <img
        :src="src"
        :height="height"
        :width="width"
        :alt="title"
    />
</template>

<script>
function getSize(size) {
    if (size === "L") {
        return "700";
    }

    if (size === "M") {
        return "340";
    }

    return "220";
}

export default {
    name: "Image",
    props: {
        src: String,
        size: String,
        title: String,
    },
    computed: {
        height() { return getSize(this.size) },
        width() { return getSize(this.size) },
    }
}
</script>

<style scoped>
img {
    object-fit: cover;
}
</style>