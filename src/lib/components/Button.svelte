<script> 

//props
//color
// is it easier and cleaner to put this in an object instead of 3 seperate variables
export let colors = {
  main: 'bg-slate-500',
  hover: 'bg-slate-700',
  active: 'bg-slate-900'
};
//text
export let btnText = 'click';
//function
export let defaultFunction = console.log('hi :)')
</script>

<!-- this isnt working -->
<button on:click = {defaultFunction} class= "{colors.main} hover:{colors.hover} active:{colors.active} rounded-md  px-4 py-2 mx-4 text-white transition ease-liner duration-150">{btnText}</button>