<script>
    import { fade } from 'svelte/transition'

    export let duration

    let imagePaths = [
      "assets/homepage/slideshow/slide1.svg",
      "assets/homepage/slideshow/slide2.svg",
      "assets/homepage/slideshow/slide3.svg",
      "assets/homepage/slideshow/slide4.svg",
      "assets/homepage/slideshow/slide5.svg"
    ];

    let currentSlide = 0;

    const nextSlide = () => {
        currentSlide++
        if (currentSlide >= imagePaths.length) {
            currentSlide = 0
        }
        timer()
    }

    const prevSlide = () => {
        currentSlide--
        if (currentSlide <= 0) {
            currentSlide = imagePaths.length - 1
        }
        timer()
    }

    const goToSlide = (i)=>{
        currentSlide = i;
        timer()
    }

    let interval
    const timer = () => {
        clearInterval(interval)
        interval = setInterval(nextSlide, duration)
    }
    timer()
</script>

<div class="slider">
    {#each imagePaths as imagePath, i}
        {#if currentSlide === i}
            <div class="slide" transition:fade>
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img
                class="image"
                src={imagePath}
                alt="Carousel Image"/>
            </div>
        {/if}
    {/each}
    <button class="next" on:click={nextSlide}>next</button>
    <button class="prev" on:click={prevSlide}>prev</button>
    <div class="nav">
        {#each imagePaths as imagePath, i}
            <div class="buttonwrap">
                <button class="bubble" on:click={()=>{
                    goToSlide(i)
                    }}
                    class:current={i === currentSlide}
                ></button>
            </div>
        {/each}
    </div>
</div>

<style>
    .slider {
        width: 80vw;
        height: 80vh;
        background-color: #222;
        position: absolute;
    }

    .slide {
        width: 80vw;
        height: 80vh;
        position: absolute;
        inset: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #708fb8;
        font-size: 7rem;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        font-weight: 300;
        clip-path: inset(0 0 0 0) /*This clips the carousel onto the size of the landing section, preventing overflow onto portfolio section*/
    }

    img {
        max-width: 90dvw;
    }

    .next, .prev {
        height: 100%;
        width: 10rem;

        position: absolute;
        z-index: 2;
        top: 0%;

        opacity: 0;
        cursor: pointer;
    }

    .next {
        right: 0px;
    }

    .prev {
        left: 0px;
    }

    .nav {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 1rem;

        height: 4rem;
        width: 100%;

        position: absolute;
        left: 0px;
        top: 0px;

        z-index: 20;
    }

    .bubble {
        width: 4rem;
        height: 0.5rem;
        padding: 0;
        border: 0;

        transition: all 0.3s ease-out;

        opacity: 0.2;
        cursor: pointer;
        z-index: 20;

        position: relative;
        top: 70vh;

        background-color: #708fb8;
    }

    .current {
        opacity: 1
    }
</style>