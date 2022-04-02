<template>
    <c-box class="server-info--container" as="button">
        <c-flex class="server-info--wrapper">
            <c-text>{{ server_info.title }}</c-text>
            <c-text>{{ server_info.players }}</c-text>
            <c-text>{{ server_info.ping }}</c-text>
        </c-flex>
    </c-box>
</template>

<script>
export default {
    // outline the button when is pressed

    props: {
        server_info: {
            type: Object,
            default: () => {},
        },
    },
};
</script>

<style>
* {
    user-select: none;
}

.server-info--container {
    width: 100%;
    height: 30px;
    background-color: rgba(40, 38, 64, 0.621) !important;
    margin-top: 4px;
    border-radius: 4px;
}

.server-info--wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 14px;
    color: #fff;
    /* center text*/
    text-align: center;
    padding: 4px;
}

.server-info--container:hover{
    background-color: rgba(35, 33, 53, 0.8) !important;
}

.server-info--container:active{
    background-color: rgba(27, 25, 40, 0.8) !important;

}

</style>