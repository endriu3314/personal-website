<script context="module">
    import Home from './pages/Home.svelte';
    import Projects from './pages/Projects.svelte';

    export const navOptions = [
        { page: 'Projects', component: Projects },
        { page: 'Home', component: Home },
    ];
</script>
