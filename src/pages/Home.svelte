<script>
    import Container from '../components/Container.svelte';
    import Language from '../components/Home/Language.svelte';
    import Title from '../components/Title.svelte';
    import { languages } from '../languages';
</script>

<div class="space-y-3">
    <Title title={'about me'} />
    <Container>
        <span class="text-white font-serif">
            17 yo old web enthusiast born in romania \n i like maths and love
            php
        </span>
    </Container>
</div>

<div class="space-y-3 mt-4">
    <Title title={'languages & technologies'} />
    <Container>
        <div class="flex flex-1 justify-start flex-wrap gap-6">
            {#each languages as language}
                <Language name={language.name} image={language.image} />
            {/each}
        </div>
    </Container>
</div>

<div class="space-y-3 mt-4">
    <Title title={'currently working on'} />
    <Container>
        <ul class="list-disc text-white ml-6 font-serif">
            <li>
                <a
                    class="text-white custom-button-underline"
                    href="https://vivatrucks.com"
                    target="_blank">viva trucking</a>
            </li>
        </ul>
    </Container>
</div>
