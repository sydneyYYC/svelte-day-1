<script>
  import Card from "../../lib/components/card.svelte";
  const cardText = {
    title: 'Placeholder Title',
    description: 'hohohohohohohahahahahahhahahha so much fun in svelte :) wowie zowie'
  }

  import Header from "../../lib/components/Header.svelte";
  const pageTitle = "This is a Gallery";
  const pageDescription = 'This is where i am working today on Nov 7'
</script>
<Header {pageTitle} {pageDescription}></Header>

<Card {...cardText}/>

<Card />

