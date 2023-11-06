<script>
  import Header from "../../lib/components/Header.svelte";

const pageTitle = "Blog Page";
const pageDescription = "This is my blog page for my Svelte Project";
const bgColor = "bg-red-200";
const name = 'Sydney';
const flexContent = "my blog is the best"
</script>

<Header {pageTitle} {pageDescription} {bgColor} />

<!-- render a hello message if the name is ash 
otherwise say GO AWAY b/c godfrey keeps trying to hack my site-->

{#if name === 'Godfrey'}
<!-- // sometimes its better to deal with the exception as the if -->
<p>GO AWAY Godfrey >:[ </p>
{:else if name === "Sydney"}
<p>hey {name}, hows the portfolio ;) ?</p>
{:else} 
<p>Hello {name}</p>
{/if}

