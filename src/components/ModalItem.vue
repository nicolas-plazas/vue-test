<template>
    <div>
        <button @click="toggle">Modal </button>
        <Teleport to="body">
            <div v-show="show" class="modal">
                <h1>Title</h1>
                <p>In dolore laborum sit do reprehenderit officia et dolore.Quis sit labore tempor nostrud ipsum magna
                    ut esse enim laboris.</p>
                <button @click="toggle">Close</button>
            </div>
        </Teleport>
    </div>
</template>

<script>
export default {
    name: 'ModalItem',
    data() {
        return {
            show: false,
        }
    },
    methods: {
        toggle: function () {
            this.show = !this.show;
        }
    }
}
</script>

<style scoped>
    .modal {
        display: flex;
        flex-direction: column;
        width: 300px;
        margin: 0 auto;
    }
</style>