<script>
    export let name;
    export let image;
</script>

<div class="mx-3">
    <h1 class="text-white text-center text-sm font-mono mb-1">{name}</h1>
    <img class="h-10 mx-auto" src={image} alt={name} />
</div>
