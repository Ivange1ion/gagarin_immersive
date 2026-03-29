<script setup></script>

<template>
    <div id="footer">
        <div id="contacts">
            8 800 555 35 35
            <br>
            <br>
            example@mail.com
        </div>
        <div id="media-links">
            <img src="" alt="телеграмм">
            <img src="" alt="вконтакте">
        </div>
    </div>
</template>

<style scoped>
    #footer{
        background-color: var(--footer);
        margin:20px;
        height: 60px;
        display: flex;
        justify-content: space-between;
        padding: 20px;
    }
    #media-links{
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }
</style>
