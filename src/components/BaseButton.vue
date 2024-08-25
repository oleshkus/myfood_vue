<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
    hovered: {
        type: Boolean,
        default: false
    },
    text: {
        type: String
    },
    color: {
        type: String,
        default: 'blue'
    },
    backgroundColor: {
        type: String,
        default: 'blue'
    },
    icon: {
        type: String
    },
    type: {
        type: String,
        default: 'button'
    },
    active: {
        type: Boolean,
        default: false
    },
    size: {
        type: String,
        default: 'normal',
        validator: (value: string) => ['narrow', 'normal', 'fixed'].includes(value)
    }
})
</script>

<template>
    <button
        :class="[
            color,
            backgroundColor,
            'rounded-lg',
            'text-md',
            active ? 'bg-opacity-10' : 'bg-opacity-0',
            {
                'px-3 py-1': size === 'narrow',
                'px-5 py-3': size === 'normal',
                'w-200': size === 'fixed',
                'px-4 py-3': !text,
                'bg-opacity-10': active
            }
        ]"
        class="hover:bg-opacity-10"
        :type="$props.type"
        @hover="hovered = !hovered"
    >
        <i
            v-if="icon"
            :class="[
                icon,
                {
                    'mr-1': !!text && size == 'narrow',
                    'mr-2': !!text && size == 'normal',
                    'fa-lg': !text
                }
            ]"
        ></i>
        {{ text }}
    </button>
</template>
<style scoped></style>
