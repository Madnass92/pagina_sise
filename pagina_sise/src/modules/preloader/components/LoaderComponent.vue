<template>

<div class="loader">
    <div></div>
    <div></div>
    <div></div>
</div>
    
</template>
<script>


export default{
    
}
</script>

<style scoped>
.loader {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 60px;
    height: 50px;

}
.loader div {
    width: 12px;
    background: blue;
    animation: loader 1.8s linear infinite;
}

.loader div:nth-child(2) {
    animation-delay: -0.25s;
}


@keyframes loader {
    0% {
        height: 12px;
    }

    25% {
        height: 50px;
    }

    50% {
        height: 10px;
    }

    75% {
        height: 25px;
    }

    100% {
        height: 12px;
    }
}


</style>