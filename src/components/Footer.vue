<template>
    <footer class="footer--container">
        <c-flex class="footer-content">
            <div class="play-button--wrapper">
                <slot></slot>
            </div>
            <div class="client-version--wrapper">
                <c-box color="grey" size="14px">Scr44gr@v0.1.0</c-box>
            </div>
        </c-flex>
    </footer>
</template>

<script>
export default {};
</script>

<style>
.footer--container {
    width: 100%;
    height: 100%;
    background-color: #32304e;
}

.footer-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

.play-button--wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 100%;
    height: 100%;
    padding: 14px;
}

.client-version--wrapper {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    height: 100%;
}
</style>