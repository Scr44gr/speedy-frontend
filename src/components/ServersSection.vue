<template>
    <c-box class="c-tab--container">
        <c-tabs
            id="c-tab--container"
            variant="unstyled"
            color="white"
            :index="0"
        >
            <c-tab-list>
                <c-tab :isDisabled="true">Speedy</c-tab>
                <c-tab>Servers</c-tab>
            </c-tab-list>

            <c-tab-panels>
                <c-tab-panel>
                    <c-flex
                        flexDirection="row"
                        bg="rgba(40, 38, 64, 0.9)"
                        w="100%"
                        p="8px"
                        h="40px"
                        justifyContent="space-between"
                    >
                        <c-text>Hostname</c-text>
                        <c-text>Players</c-text>
                        <c-text>Ping</c-text>
                    </c-flex>
                    <c-box id="server-description--box">
                        <ServerItem
                            v-for="server_info in servers[currentTab]"
                            :key="server_info.id"
                            :server_info="server_info"
                        />
                    </c-box>
                </c-tab-panel>
                <c-tab-panel>
                    <c-flex
                        flexDirection="row"
                        bg="rgba(40, 38, 64, 0.9)"
                        w="100%"
                        p="8px"
                        h="40px"
                        justifyContent="space-between"
                    >
                        <c-text>Hostname</c-text>
                        <c-text>Players</c-text>
                        <c-text>Ping</c-text>
                    </c-flex>
                    <c-box id="server-description--box">
                        <ServerItem
                            v-for="server_info in servers[currentTab]"
                            :key="server_info.id"
                            :server_info="server_info"
                        />
                    </c-box>
                </c-tab-panel>
            </c-tab-panels>
        </c-tabs>
    </c-box>
</template>

<script>
import ServerItem from "./ServerItem.vue";

export default {
    props: {
        servers: {
            type: Object,
            default: () => {},
        },
    },
    components: {
        ServerItem,
    },

    data: () => ({
        currentTab: 0,
    }),
};
</script>

<style>

#c-tab--container {
    border-radius: 5px;
}

#server-description--box {
    padding: 4px;
    background-color: rgba(50, 48, 78, 0.8);
    height: 400px;
    overflow-y: hidden;
    overflow-x: hidden;
    resize: horizontal;
    width: 800px;
    max-width: 1000px;
    min-width: 500px;
    min-height: 400px;
    max-height: 550px;
    border-radius: 0px 0px 5px 5px;
}

#c-tab--container div button {
    background-color: #e16969a9;
    margin-right: 4px;
}
</style>