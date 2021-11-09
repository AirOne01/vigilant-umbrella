<main>
    <div id="title">
        <img alt="Alternexus title"/>
    </div>
    <div id="header">
        <div>El 1</div>
        <div>El 2</div>
        <div>El 3</div>
    </div>
    <div id="pfp"></div>
</main>

<style>
    main {
        position: fixed;
        height: 100%;
        width: 100%;
        left: 0px;
        top: 0px;
        background-color: black;
    }

    #header {
        /* display & sizes */
        left: 12vw;
        top: 0px;
        display: flex;
        height: 7vh;
        width: calc(88vw - 15vh);
        margin: 0px;
        position: fixed;
        /* flex */
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        /* other */
        background-color: #001f3f;
    }

    #header * {
        color: white;
        background-color: rgba(255, 255, 255, 0.151);
    }

    #pfp {
        /* flex */
        justify-self: flex-start;
        /* height ratio and position */
        height: 15vh;
        aspect-ratio: 1/1;
        position: fixed;
        top: 0;
        right: 0;

        background-color: #001f3f;
        border-bottom-left-radius: 10%;
    }

    #title {
        display: block;
        width: 12vw;
        aspect-ratio: 16/9;
        background-color: #001f3f;
        border-bottom-right-radius: 1.2vh;
    }
</style>