<script>
  import Button from "../lib/components/Button.svelte";
import Header from "../lib/components/Header.svelte";
import Card from "../lib/components/card.svelte";

let pageTitle = 'Hello!';
let pageDescription = "Welcome to the home page. This is my first svelte project :)"
const bgColor = "bg-green-200"

  // let dailyContent = "Hello!"
  // let description = "this is my first svelte project :) yay"

  let hellos = [
    {title: "this is my first card", description: "keyboard cat"},
    {title: "this is my second card", description: "bongo cat"},
    {title: "this is my third card", description: "balthazar momalthizar fefifofalthizar the |||"}
]


</script>

<Header {pageTitle} {pageDescription} {bgColor}/>
<!-- <h1 class="text-3xl text-center mt-4">Welcome to SvelteKit Dem0</h1>
<section class="font-semibold text-center p-4 mt-4">
<p>{dailyContent}</p>
<p>{description}</p>
</section> -->


<!-- for each loop -->
{#each hellos as card}
<Card {...card}/>

{/each}

<Button></Button>

<!-- note using a for each loop: 

the object needs to use the same key value pairs as the component to work

the array needs to be named the same as in the card as it is originally and the passed values GO FIRST 

the second value is a placeholder to use in the each and in the spread operator {...[value]} the 3 dots indicate the spread operator 

for example in this instance 'card' is a placeholder and it can be anything technically as long as its used in those two places -->