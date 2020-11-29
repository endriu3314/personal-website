<script>
    import { createEventDispatcher, each } from 'svelte/internal';
    import { navOptions } from '../Nav.svelte';

    const dispatch = createEventDispatcher();
    let selectedIndex = 0;

    const changeComponent = (event) => {
        selectedIndex = event.srcElement.id;
        dispatch('message', {
            component: navOptions[event.srcElement.id],
        });
    };
</script>

<style>
    .selected {
        border-color: #aaa #565656 #565656 #aaa;
        text-shadow: 3px 3px #4c4c4c;
        border: 1px solid;
    }
</style>

<nav class="mx-auto justify-center">
    <div class="flex items-center justify-between h-16">
        <div class="flex-1 flex items-center justify-between sm:items-stretch">
            <div class="flex-shrink-0 flex items-center">
                <span
                    class="text-white text-lg font-bold subpixel-antialiased">andreicroitoru</span>
            </div>
            <div class="hidden sm:block sm:ml-6">
                <div class="flex space-x-4">
                    {#each navOptions as option, index}
                        <button
                            class={index == selectedIndex ? 'px-3 py-2 text-sm text-white lowercase font-mono focus:outline-none selected' : 'px-3 py-2 text-sm text-white lowercase font-mono focus:outline-none custom-button-border'}
                            on:click={changeComponent}
                            id={index}
                            role="tab">
                            {option.page}
                        </button>
                    {/each}
                </div>
            </div>
            <div class="sm:block sm:ml-6">
                <div class="flex">
                    <a
                        href="https://github.com/endriu3314"
                        target="_blank"
                        class="px-3 py-2 text-sm text-white font-medium subpixel-antialiased custom-button-underline">
                        GitHub
                    </a>
                    <a
                        href="https://www.linkedin.com/in/andrei-croitoru-rusan-2b81ab15a/"
                        target="_blank"
                        class="px-3 py-2 text-sm text-white font-medium subpixel-antialiased custom-button-underline">
                        LinkedIn
                    </a>
                    <a
                        href="https://www.instagram.com/endriu.xx/"
                        target="_blank"
                        class="px-3 py-2 text-sm text-white font-medium subpixel-antialiased custom-button-underline hidden sm:block">
                        Instagram
                    </a>
                </div>
            </div>
        </div>
    </div>
</nav>
