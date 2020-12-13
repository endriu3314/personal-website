<script context="module">
    import Home from './pages/Home.svelte';
    import Projects from './pages/Projects.svelte';

    export const navOptions = [
        { page: 'Home', component: Home },
        { page: 'Projects', component: Projects },
    ];
</script>
