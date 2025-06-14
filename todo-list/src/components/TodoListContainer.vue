<script setup>
    // import { ref } from 'vue';
    // const showEmptyListSection = ref(false);
</script>

<template>
    <div class="todo-list-container">

        <div  class="empty-list">
            <h2 class="empty-list-title">No tasks found!</h2>
            <p class="empty-list-subtitle">Add your first task to get started.</p>
        </div>

        <ul class="todo-list">
            <li class="todo-item">
                <span class="todo-item-text">Todo item</span>
                <div class="todo-actions">
                    <button class="action-btn">edit</button>
                    <button class="action-btn">delete</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
    .todo-list-container{
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(20px);
        border-radius: 15px;
        padding: 18px;
        border: 1px solid rgba(255, 255, 255, 0.2);
        box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        max-height: 600px;
        overflow-y: scroll;
    }
    .todo-list-container::-webkit-scrollbar{
        display: none;
    }
    .empty-list{
        text-align: center;
        padding: 50px 0px;
        color: rgba(255, 255, 255, 0.8);
        font-weight: bold;
        letter-spacing: 1px;
    }
    .empty-list-title{
        font-size: 25px;
        margin-bottom: 10px;
    }
    .empty-list-subtitle{
        font-size: 18px;
    }
    .todo-list{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
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

