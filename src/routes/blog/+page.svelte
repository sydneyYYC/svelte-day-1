<script>
  import Header from "../../lib/components/Header.svelte";

const pageTitle = "Blog Page";
const pageDescription = "This is my blog page for my Svelte Project";
const bgColor = "bg-red-200";

let userLogin = true;
let user = {
  name:'Ash',
  login: true,
}

function greet() {
  if(userLogin){
    alert('Hello :)');
  }
}

function userLoginToggle() {
  // this changes the login state from true to false with the '!' conditional 
  return user.login =!user.login;
};
</script>

<Header {pageTitle} {pageDescription} {bgColor} flexContent>This is for the Flexbox</Header>

{#if user.name === 'Godfrey'}
<p>Stop trying to hack my site</p>
{:else if user.name === 'Sydney'}
<p>You're doing great! :D</p>
{:else}
<p>Good morning {user.name}!</p>
{/if}
<!-- buttons for alert -->
<!-- note - your event will still need a function to run  -->

<h2 class="text-3xl m-4">Toggles</h2>
<button on:click={greet} class="rounded-md bg-red-500 px-4 py-2 mx-4 text-white transition ease-liner duration-150 hover:bg-red-700 active:bg-red-900">Send Alert</button>
<button on:click={userLoginToggle} class="rounded-md bg-blue-500 px-4 py-2 mx-4 text-white transition ease-liner duration-150 hover:bg-blue-700 active:bg-blue-900">Toggle User Login</button>

<!-- component events and event props-->
{#if user.login=== true}
<p> Welcome to the site, {user.name}</p>
<p class="text-2xl m-4">{user.login}</p>
{/if}

