<script>
  import ListItem from "../../lib/components/ListItem.svelte";
let listItems = ['har', 'dar', 'lar', 'car', 'var'];
let secondList = [
  {name:'Alfred', species:'Dog'},
  {name:'Elvira', species:'cat'},
  {name:'sally', species:'crow'}
];
</script>

<header class="my-4 text-center text-5xl">
  <h1>About Page</h1>
</header>

<section class="text-center">
  <h2 class="text-3xl">Our Example List</h2>
  <ul class=" ml-8">
    {#each listItems as item, i}
    <ListItem listStyles="bg-amber-50">{item}</ListItem>
    {/each}

    <!-- you can rewrite default styles by using the styles tag from component and adding your override with ="[style]" -->
  </ul>
</section>

<section>
  <h2 class="text-3xl ml-8">Animals</h2>
  <ul class="ml-8">
    {#each secondList as {name, species}}
    <ListItem listStyles>{name} is a {species}</ListItem>
    {/each}
  </ul>  
</section>