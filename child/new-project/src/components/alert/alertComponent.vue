<script setup>
    import { defineProps } from 'vue'

    defineProps({
        typeAlert: String,
        title: String,
        message: String,
        isVisible: Boolean,
    })
</script>

<template>
    <section v-if="isVisible" class="alert" :class="`alert-${typeAlert}`">
        <div class="message-area">
            <span>{{title}}</span>: <span> {{message}}</span>
        </div>
        <div class="close-area">
            <button @click="$emit('close', $event)">X</button>
        </div>
    </section>  
</template>
