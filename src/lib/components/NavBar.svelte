<script>
  const navItems = [
    {name: 'home', href: "/"},
    {name:'about', href:'/about'},
    {name:'gallery', href: '/gallery'}
  ];
</script>

<header class="bg-slate-950 text-slate-50 flex justify-between px-4">
  <div>
    logo
  </div>
  <nav>
    <ul class="flex justify-around px-2">
      {#each navItems as {name, href}}
      <li class="px-2"><a {href}>{name}</a></li>
      {/each}
    </ul>
  </nav>
</header>