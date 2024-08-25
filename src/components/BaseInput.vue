<script>
export default {
    props: {
        type: {
            type: String,
            default: 'text'
        }
    }
}
</script>

<template>
    <input :type="type" />
</template>

<style scoped></style>
