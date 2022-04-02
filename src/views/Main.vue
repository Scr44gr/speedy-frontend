<template>
    <c-box class="main-app--container">
        <div class="main-app--wrapper">
            <c-flex class="app-section--container">
                <Body>
                    <ServerSection :servers="this.servers" />
                </Body>
            </c-flex>
            <Footer>
                <PlayButton label="Play Now" :onClick="() => {}" />
            </Footer>
        </div>
    </c-box>
</template>

<script>
import Body from "../components/Body.vue";
import PlayButton from "../components/PlayButton.vue";
import Footer from "../components/Footer.vue";
import ServerSection from "../components/ServersSection.vue";

export default {
    components: {
        Body,
        PlayButton,
        ServerSection,
        Footer,
    },

    data: () => {
        return {
            servers: {
                0: [
                    {
                        title: "Test Server",
                        players: 0,
                        ping: "100ms",
                    },
                    {
                        title: "Test Server 2",
                        players: 100,
                        ping: "200ms",
                    },
                ],
            },
        };
    },
};
</script>

<style>
.main-app--container {
    width: 100%;
    height: 100vh;
    background-image: url("https://as01.epimg.net/meristation/imagenes/2021/07/26/noticias/1627309597_830619_1627309735_noticia_normal.jpg");
    flex-direction: column;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    /* filter background image */
}

.main-app--wrapper {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    background-color: rgba(50, 48, 78, 0.7);
}
</style>