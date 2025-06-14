<scirpt>

</scirpt>

<template>
    <input class="task-input" type="text" placeholder="type here ...">
</template>

<style scoped>
    .task-input{
        flex: 1;
        padding: 16px;
        background: rgba(255, 255, 255, 0.1);
        border: 1px solid rgba(255, 255, 255, 0.3);
        border-radius: 14px;
        backdrop-filter: blur(10px);
        color: #fff;
        font-size: 17px;
    }
    .task-input::placeholder {
        color: #fff;
        font-size: 17px;
    }
</style>
