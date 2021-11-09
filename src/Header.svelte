<script lang="ts">
    export let pfp_url: string;
    export let pfp_name: string;
</script>

<main>
    <span id="title">
        <img alt="Alternexus title"/>
    </span>
    <span id=header>
        test
    </span>
    <span id="pfp" src={pfp_url}>
        <img alt="{pfp_name}"/>
    </span>
</main>

<style>
    main {
        width: 100%;
        height: 15vh;
        left: 0;
        top: 0;
        position: fixed;
    }

    #title {
        float: left;
        height: 12vh;
        aspect-ratio: 16/9;
        background-color: #001219;
        position: relative;
    }

    #header {
        float: left;
        display: flex;
        width: calc(100vw - 12vh*16/9 - 15vh);
        height: 7vh;
        background-color: #001219;
    }

    #pfp {
        float: right;
        height: 15vh;
        aspect-ratio: 1/1;
        background-color: #001219;
    }
</style>