<script>
    import Navbar from "../components/Navbar.svelte";

    // Conditional html
    let num = 5;
    let showModal = true;

    // Conditional style
    let advertisement = true;
</script>

<div class="content">
    <Navbar />

    <div class="contentAlignment">

        <div class="box">
            {#if num > 20}
                <p>Greater than 20</p>
            {:else if num > 5}
                <p>Greater than 5</p>
            {:else}
                <p>Not greater than 5</p>
            {/if}
        </div>

        <div class="box">
            {#if showModal}
                <div class="backdrop" class:advertisement={advertisement}>
                    <div class="modal">
                        <p>Sign in for offers!</p>
                    </div>
                </div>
            {/if}
        </div>
    
    </div>
</div>

<style>
    .content {
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
    }

    .contentAlignment {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-evenly;
    }

    .box {
        width: 35%;
        height: 95%;
        background-color: rgb(102, 180, 92);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 1.1rem;
    }

    p {
        font-size: 1.5em;
    }

    .backdrop {
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.7);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .modal {
        width: 35%;
        height: 12%;
        background-color: white;
        display: flex;
        border-radius: 5%;
        text-align: center;
    }

    .advertisement .modal {
        background-color: crimson;
    }
</style>
