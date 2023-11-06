<!-- standard page header -->

<!-- 1. consistent titles (prop)
2. consistent layout (markup)
3. page specific color (props)
4. room for flexibility (slots) -->

<script>
export let pageTitle;
export let pageDescription;
export let bgColor = "bg-blue-200";
export let flexContent = false;
</script>

<header class=" min-w-full flex flex-col items-center p-2 {bgColor}">

<h1 class="text-4xl p-2 mx-4 font-bold">{pageTitle}</h1>

<p class="text-lg p-2">{pageDescription}</p>
{#if flexContent === true}
<div class="bg-white text-blue-600 rounded-lg p-4">
<slot />
</div>
{/if}
</header>