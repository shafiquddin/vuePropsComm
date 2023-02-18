<template>
    <dialog open>
        <slot></slot>
    </dialog>
</template>

<style scoped>
dialog{
    margin:0;
    padding:20px;
    background-color: whitesmoke;
    box-shadow: 0 2px 8px rgba(0,0,0,0.26);
    position: fixed;
    top:20vh;
    left:30%;
    width:40%;
}
</style>