<script>
  import Header from "../../lib/components/Header.svelte";

const pageTitle = "Blog Page";
const pageDescription = "This is my blog page for my Svelte Project";
const bgColor = "bg-red-200";

let userLogin = true;

function greet() {
  if(userLogin){
    alert('Hello :)');
  }
}

function userLoginToggle() {
  // this changes the login state from true to false with the '!' conditional 
  return userLogin =!userLogin;
};
</script>

<Header {pageTitle} {pageDescription} {bgColor} flexContent>This is for the Flexbox</Header>


<!-- buttons for alert -->
<!-- note - your event will still need a function to run  -->
<button on:click={greet} class="rounded-md bg-red-500 px-4 py-2 mx-4 text-white transition ease-liner duration-150 hover:bg-red-700 active:bg-red-900">Send Alert</button>
<button on:click={userLoginToggle} class="rounded-md bg-blue-500 px-4 py-2 mx-4 text-white transition ease-liner duration-150 hover:bg-blue-700 active:bg-blue-900">Toggle User Login</button>

<!-- component events and event props-->
<p class="text-5xl m-4">{userLogin}</p>