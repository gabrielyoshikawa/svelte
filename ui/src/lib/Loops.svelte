<script>
    import Navbar from "../components/Navbar.svelte";

    let fruits = [
        { id: 1, name: "Banana", color: "yellow", quantity: 24 },
        { id: 2, name: "Avocado", color: "green", quantity: 15 },
        { id: 3, name: "Tangerine", color: "orange", quantity: 56 }
    ];
</script>

<div class="content">
    <Navbar />

    <div class="box">
        <!-- Good practice - pass a unique value as parameter -->
        {#each fruits as fruit (fruit.id)}
            <p>{fruit.name} - {fruit.quantity} units in stock.</p>
        {:else}
            <p>We sell it all! No fruit available in stock.</p>
        {/each}
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
        background-color: rgb(204, 55, 55);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 1.1rem;
    }

    p {
        font-size: 1.5em;
    }
</style>
