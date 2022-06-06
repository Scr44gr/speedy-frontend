<template>
    <c-box class="play-button--container">
        <c-button class="play-button" @click="onClick" h="60px" w="200px" fontSize="28px">
            {{ label }}
        </c-button>
    </c-box>
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            default: "Play Now",
        },
        onClick: {
            type: Function,
            default: () => {},
        },
    },
};
</script>

<style>
.play-button {
    background-color: #fffb95!important;
    box-shadow: #fffb95 0px 0px 8px;
}
</style>