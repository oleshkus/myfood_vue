<template>
    <div>
        <button @click="showModal = true">Открыть модальное окно</button>

        <div v-if="showModal" class="modal">
            <div class="modal-wrapper flex justify-center items-center flex-col mt-[5%] gap-0">
                <div
                    class="modal-header flex justify-between items-center text-xl bg-slate-300 w-[90%] max-w-[40rem] rounded-t-md px-5 py-3 gap-60"
                >
                    <h2>{{ title }}</h2>
                    <button @click="showModal = false">&times</button>
                </div>
                <div class="modal-content w-[90%] max-w-[40rem] bg-slate-50 px-5 py-3 rounded-b-md">
                    <slot></slot>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showModal: false
        }
    },
    props: {
        title: {
            type: String
        }
    }
}
</script>

<style>
.modal {
    display: block;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(1px);
}

.close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close:hover,
.close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}
</style>
