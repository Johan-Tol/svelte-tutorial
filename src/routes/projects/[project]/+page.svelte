<script>
    import Navbar from '$lib/components/+navbar.svelte';
    import Projects from '$lib/assets/projects.json';
    let { params } = $props();
    let projectname = params.project;
    let project = Projects.projects.find((project) => {
        return project.title === projectname
    });
    console.log(project);
</script>

<Navbar/>

<h1>{project.title}</h1>
<h3>Project description</h3>
<p>{project.description}</p>
<h3>techstack</h3>
<li>
    {#each project.techstack as type}
    <ul>{type}</ul>
    {/each}
</li>
<h3>start date</h3>
<p>{project.start_date}</p>

<style>
</style>
