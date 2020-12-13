<script>
    import Container from '../components/Container.svelte';
    import Project from '../components/Projects/Project.svelte';
    import Title from '../components/Title.svelte';
    import { projects } from '../projects';
</script>

<div class="space-y-3">
    <Title title={'projects'} />
    <Container>
        <div class="flex flex-1 justify-center flex-wrap gap-4">
            {#each projects as project}
                <Project name={project.name} image={project.image} description={project.description} url={project.href} />
            {/each}
        </div>
    </Container>
</div>
