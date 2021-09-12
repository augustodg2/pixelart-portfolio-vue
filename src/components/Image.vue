<template>
    <img
        :src="src"
        :height="height"
        :width="width"
        :class="classname"
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
        classname() { return `size-${this.size.toLowerCase()}`}
    }
}
</script>

<style scoped>
img {
    object-fit: cover;
}

@media screen and (max-width: 700px) {
    img.size-l {
        width: 100vw;
        height: 100vw;
    }
    img.size-m {
        width: calc(50vw - 5px);
        height: calc(50vw - 5px);
    }
    img.size-s {
        width: calc(33vw - 2.5px);
        height: calc(33vw - 2.5px);
    }
}
</style>