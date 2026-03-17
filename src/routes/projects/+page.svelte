<script>
    import Navbar from '$lib/components/+navbar.svelte';
    import Projects from '$lib/assets/projects.json';
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

<h3>Projects</h3>
<li>
    {#each Projects.projects as project}
    <ul><a href="/projects/{project.title}">{project.title}</a></ul>
    {/each}
</li>

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
