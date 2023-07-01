<script>
    let name = "Name";
    let beltColor = "Black";

    const updateBeltColorButton = () => {
        beltColor = "Orange";
    };

    const updateBeltColorInput = (event) => {
        beltColor = event.target.value;
    };

    import Navbar from "../components/Navbar.svelte";

</script>

<div class="content">

    <Navbar />

    <div class="box">
        <p>Welcome {name}!</p>
        <p style="color: {beltColor};">Your belt color is: {beltColor}</p>
        <button on:click={updateBeltColorButton}>Click for update your belt color to Orange</button>
        <!-- One way binding -->
        <!-- <input type="text" placeholder="Type for update your belt color" on:input={updateBeltColorInput} value={beltColor} /> -->
        <!-- Two way binding -->
        <input type="text" bind:value={beltColor} />
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
        background-color: lightblue;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 1.1rem;
    }

    p {
        font-size: 2em;
    }

    button {
        width: 40%;
        height: 7%;
        background-color: orange;
        border: none;
        border-radius: 3%;
    }

    button:hover {
        cursor: pointer;
        background-color: peru;
    }
    
    input {
        margin-top: 1rem;
        height: 5%;
        width: 40%;
        border: none;
        background-color: lightgreen;
    }
</style>
