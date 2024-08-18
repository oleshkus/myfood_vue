<script setup lang="ts">
import BaseButton from '../components/BaseButton.vue'
</script>
<template>
    <div class="about">
        <h1>This is an about page</h1>
        <base-button
            type="submit"
            text="Конфиденциальность"
            color="text-blue-400"
            background-color="bg-blue-400"
            icon="fa-solid fa-thumbs-up"
            size="narrow"
        />

        <div class="flex justify-center">
            <base-button
                type="button"
                color="text-blue-400"
                background-color="bg-blue-400"
                icon="fa-solid fa-magnifying-glass"
                size="normal"
                active
            />
            <base-button
                type="submit"
                text="Click me"
                color="text-blue-400"
                background-color="bg-blue-400"
                icon="fa-solid fa-thumbs-up"
                size="normal"
                outline
            />
        </div>
    </div>
</template>

<style>
@media (min-width: 1024px) {
    .about {
        min-height: 100vh;
        display: flex;
        align-items: center;
        flex-direction: column;
    }
}
</style>
