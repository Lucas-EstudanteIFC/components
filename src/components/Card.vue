<script setup>
defineProps({
    title: String,
    required: true
})
</script>
<template>
    <div class="card">
        <h1>{{ title }}</h1>
        <slot>Conteúdo genérico do Slot</slot>
    </div>
</template>
<style scoped>
.card {
    padding: 20px;
    border: 1px solid gray;
    border-radius: 5px;
    box-shadow: 3px 3px 2px 2px gray;
}
</style>