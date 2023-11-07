<script>
  import Card from "../../lib/components/card.svelte";
  const cardText = {
    title: 'Placeholder Title',
    description: 'hohohohohohohahahahahahhahahha so much fun in svelte :) wowie zowie'
  }

  import Header from "../../lib/components/Header.svelte";
  const pageTitle = "This is a Gallery";
  const pageDescription = 'This is where i am working today on Nov 7'

  // slide array to loop through
const slideArr = [1, 2, 3, 4, 5];

// current index counter
let currentSlide = 0;

// max length of the array
const maxLength = slideArr.length - 1;

const displayCurrentSlide = document.querySelector('#current-slide');

const displayCurrentSlideIndex = document.querySelector("#current-slide-index");

// broken somehow
function nextSlide() {
  if (currentSlide === maxLength) {
    currentSlide = 0;
    currentSlideContent = (slideArr[currentSlideIndex]);
    
  } else {  
  currentSlide++;
    currentSlideContent = (slideArr[currentSlideIndex]);
  }
}

    // previous slide function
  function prevSlide() {
  if (currentSlide === 0) {
    currentSlide = maxLength;
    currentSlideContent = (slideArr[currentSlideIndex]);
  } else {
  currentSlide--;
  currentSlideContent = (slideArr[currentSlideIndex]);
  }
}


</script>
<Header {pageTitle} {pageDescription}></Header>

<Card {...cardText}/>

<Card />

<!-- todo show slide index and slide content -->
<section>
  <h1 id="current-slide">0</h1>
  <h2>Current Index: <span id="current-slide-index"></span></h2>
  <button id="next-slide" on:click={nextSlide} >Next</button>
  <button id="prev-slide" on:click={prevSlide} >Prev</button>
</section>

