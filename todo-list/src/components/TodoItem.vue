<script setup>
    import { defineProps, defineEmits } from 'vue';
    const props = defineProps({
        taskName: {
            type: String
        }
    });

    // declaring events that emit
    const emit = defineEmits(['delete-task']);


</script>

<template>
    <li class="todo-item">
        <span class="todo-item-text">{{ taskName }}</span>
        <div class="todo-actions">
            <button class="action-btn">Edit</button>
            <button class="action-btn" @click="emit('delete-task')">Delete</button>
        </div>
    </li>
</template>

<style scoped>
    .todo-item{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 18px;
        border:1px solid rgba(255, 255, 255, 0.3);
        backdrop-filter: blur(10px);
        border-radius: 15px;
    }
    .todo-item-text{
        font-size: 18px;
        font-weight: bold;
        letter-spacing: 1px;
    }
    .todo-actions{
        display: flex;
        gap: 8px;
        align-items: center;
        justify-content: center;
    }
    .action-btn{
        padding: 12px 16px;
        background:#552275c0 ;
        opacity: 0.9;
        color: white;
        border-radius: 14px;
        font-size: 17px;
        font-weight: bold;
        letter-spacing: 1px;
        box-shadow: 0 1px 10px rgba(255, 255, 255, 0.2);
    }
    .action-btn:active {
        transform: scale(0.99);
    }
</style>