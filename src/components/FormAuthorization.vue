<script>
import BaseInput from '../components/BaseInput.vue'
import BaseModal from '../components/BaseModal.vue'
export default {
    components: {
        BaseInput,
        BaseModal
    }
}
</script>

<template>
    <div class="flex justify-center items-center flex-col">
        <label for="emailInput" class="flex justify-start flex-col">
            Email
            <base-input id="emailInput" type="text" class="h-7 p-2 bg-sky-100" />
        </label>

        <label for="passwordInput"></label>
        <base-input id="passwordInput" type="password" class="h-6 p-1" />

        <base-button
            type="submit"
            text="Войти"
            color="text-blue-400"
            background-color="bg-blue-400"
            icon="fa-solid fa-thumbs-up"
            size="narrow"
        />
    </div>
</template>

<style scoped></style>
