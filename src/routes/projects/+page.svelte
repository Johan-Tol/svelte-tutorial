<script>
    import Navbar from '$lib/components/+navbar.svelte'
    let Text = $state('Default text');
</script>

<Navbar/>

<h1>dit is om te kijken naar sveltekit hoe het werkt</h1>

<div>
    <div class="right">
        <h3>{Text}</h3>
    </div>
</div>
<input type="text" bind:value={Text}>
<button onclick={() => Text = "Default text"}>reset</button>

<style>
    div {
        width: 50%;
        display: flex;
        justify-content: center;
    }

    .right {
        justify-content: right;
    }
</style>
