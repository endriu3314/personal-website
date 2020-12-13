<script>
    export let image;
    export let name;
    export let url;
    export let description;
</script>

<style>
    .custom-container {
        border: 1px solid;
        border-color: #aaa #565656 #565656 #aaa;
    }
</style>

<div class="max-w-sm custom-container">
    <div class="max-w-sm">
        <img class="h-20" src={image} alt={name} />
    </div>
    <a href={url} target="_blank" class="text-4xl tracking-tighter lowercase font-serif text-white px-2 custom-button-underline">
        {name}
    </a>
    <div class="text-white px-2 font-serif pb-2">
        {description}
    </div>
    <div class="max-w-sm px-2">
        <slot />
    </div>
</div>