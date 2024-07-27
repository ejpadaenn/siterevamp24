<script>
    import Carousel from '$lib/components/Carousel.svelte'

    import { onMount } from 'svelte'
    
    onMount(() => {
        console.log('attaching scrollreveal.js');
        const script = document.createElement('script');
        script.src = 'src/lib/scrollreveal.js';
        script.async = true;
        document.body.appendChild(script);
    });
</script>

<html lang="en">
    <div class="mcontainer">
        <h1>Announcements</h1>
        <div class="carousel">
            <Carousel 
            duration="5000"/>
        </div>
    </div>
</html>

<style>
    html {
        height: 110vh;
        min-height: 110vh;
        width: 100vw;
        max-width: 100%;
        max-height: 110vh;

        background-color: white;
    }

    .mcontainer {
        height: 110vh;

        margin-top: 5vh;

        display: grid;
        grid-template-columns: 5% 1fr 5%;
        grid-template-rows: 1fr 1fr;

        align-items: center;
        justify-items: center;
    }

    .carousel {
        height: inherit;
        grid-column: 2;
        grid-row: 1;

        display: grid;
        grid-template-columns: inherit;
        grid-template-rows: 1fr 1fr;

        align-items: center;
        justify-items: center;

    }

    h1 {
        grid-row: 1;
        grid-column: 2;
        align-self: start !important;
        justify-self: center !important;

        font-family: "Poppins", sans-serif;
        font-weight: 700;
        font-style: normal;
        font-size: 4rem;

        margin-bottom: 0;

        color: #252626;
    }

    .reveal {
        position: relative;
        transform: translateY(50px);
        opacity: 0;

        transition: all 1s ease;
    }
</style>