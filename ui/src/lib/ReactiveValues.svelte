<script>
    import Navbar from "../components/Navbar.svelte";

    let firstName = "John";
    let lastName = "Doe";
    let beltColor = "Black";

    // Reactive value
    $: fullName = `${firstName} ${lastName}`;

    // Reactive statement
    $: {
        console.log(fullName)
    }

</script>

<div class="content">
    <Navbar />

    <div class="box">
        <!-- <p>{firstName} {lastName} - your belt color is: {beltColor}</p> -->
        <!-- Work the same way as above, but using reactive value :D -->
        <p>{fullName} - your belt color is: {beltColor}</p>
        <input type="text" bind:value={firstName} />
        <input type="text" bind:value={lastName} />
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
        background-color: rgb(130, 97, 163);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 1.1rem;
    }

    p {
        font-size: 2em;
    }

    input {
        margin-top: 1rem;
        height: 5%;
        width: 40%;
        border: none;
        background-color: rgb(223, 149, 210);
    }
</style>
