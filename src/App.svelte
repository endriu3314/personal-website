<script>
    import Navbar from './components/Navbar.svelte';
    import { navOptions } from './Nav.svelte';
    import Tailwindcss from './Tailwindcss.svelte';

    let selected = navOptions[0];
    const handleTabChange = (event) => {
        selected = event.detail.component;
    };
</script>

<style>
    main {
        cursor: crosshair;
    }
</style>

<Tailwindcss />
<main class="bg-black py-10 min-h-screen">
    <div class="max-w-xs md:max-w-2xl lg:max-w-4xl space-y-5 mx-auto">
        <div class="pb-4">
            <Navbar on:message={handleTabChange} />
        </div>
        <svelte:component this={selected.component} />
    </div>
</main>
