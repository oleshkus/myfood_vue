<script>
import BaseButton from '@/components/BaseButton.vue'
import FormAuthorization from '@/components/FormAuthorization.vue'
import BaseModal from '@/components/BaseModal.vue'
export default {
    components: {
        BaseModal,
        BaseButton,
        FormAuthorization
    }
}
</script>
<template>
    <div class="about">
        <base-modal title="Создание модального окна">
            <form-authorization />
        </base-modal>

        <h1 class="bg-amber-600 rounded-full p-5 text-white text-2xl">This is an about page</h1>
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
                size="narrow"
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
