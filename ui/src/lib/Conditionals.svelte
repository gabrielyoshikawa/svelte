<script>
    import Navbar from "../components/Navbar.svelte";

    let num = 5;
</script>

<div class="content">
    <Navbar />

    <div class="box">
        {#if num > 20}
            <p>Greater than 20</p>
        {:else if num > 5}
            <p>Greater than 5</p>
        {:else}
            <p>Not greater than 5</p>
        {/if}
        
    </div>
</div>

<style>
    .content {
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    .box {
        width: 35%;
        height: 85%;
        background-color: rgb(102, 180, 92);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 1.1rem;
    }

    p {
        font-size: 1.5em;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
            Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue",
            sans-serif;
    }
</style>
