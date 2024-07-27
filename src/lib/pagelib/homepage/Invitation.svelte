<script>
    import { onMount } from 'svelte'
    
    onMount( () => {
        console.log('attaching scrollreveal.js');
        const script = document.createElement('script');
        script.src = 'src/lib/scrollreveal.js'; // might be outdated so check for an update can link
        script.async= true;
        document.body.appendChild(script);
    });
</script>
<!--add a background image to make more interesting-->
<html lang="en">
    <div class="midpagecontainer">
        <div class="section1 reveal">
            <h1 class="section1text">Find a church near you!</h1>
            <div class="attendbutton">
                <a href="/churches"><p class="plink">Locations</p></a>
            </div>
        </div>
        <div class="section2 reveal">
            <h2>...can't attend our services?</h2>
            <div class="livebutton">
                <a href="https://www.facebook.com/cnci.newzealand"><p class="pother">Join us online!</p></a>
            </div>
        </div>
    </div>
</html>

<style>
    html {
        height: 80vh;
        width: 100vw;
        max-width: 100%;

        background-color: #708fb8;
    }

    .midpagecontainer {
        height: 80vh;

        display: grid;
        grid-template-columns: 15% 1fr 15%;
        grid-template-rows: 1fr 1fr;
    }

    .section1 {
        height: 10vh;

        grid-column: 2 / 3;
        grid-row: 1 / 2 !important;

        align-self: start;
        justify-self: center;
        
        display: grid;
        grid-template-rows: 1fr 1fr;

        place-items: center;
    }

    .attendbutton {
        width: 10rem;
        height: 3rem;

        background-color: transparent;
        border: 2px solid white;

        cursor: pointer;

        display: flex;
        align-items: center;
        justify-content: center;

        transition: all 0.4s ease-out;
    }

    .attendbutton:hover {
        background-color: white;
    }

    .attendbutton:hover > a {
        color: #708fb8
    }

    .livebutton {
        width: 10rem;
        height: 3rem;

        background-color: transparent;
        border: 2px solid white;

        cursor: pointer;

        display: flex;
        align-items: center;
        justify-content: center;

        transition: all 0.4s ease-out;
    }

    .livebutton:hover {
        background-color: white;
    }

    .livebutton:hover > a {
        color: #708fb8
    }

    .section2 {
        height: 10vh;

        grid-column: 2 / 3;
        grid-row: 2 / 3 !important;

        align-self: start;
        justify-self: center;

        display: grid;
        grid-template-rows: 1fr 1fr;

        place-items: center;
    }

    h1 {
        font-family: "Poppins", sans-serif;
        font-weight: 700;
        font-style: normal;
        font-size: 3rem;

        line-height: 6rem;
        margin-bottom: 0;

        color: #252626;
    }

    h2 {
        font-family: "Poppins", sans-serif;
        font-weight: 600;
        font-style: normal;
        font-size: 2.5rem;

        color: #252626;
    }

    p {
        font-family: "Poppins", sans-serif;
        font-weight: 500;
        font-style: normal;
    }

    a {
        text-decoration: none;
        color: white;

        transition: all 0.4s ease-out;
    }

    .reveal {
        position: relative;
        transform: translateY(50px);
        opacity: 0;

        transition: all 1s ease;
    }

    :global(.reveal.active) {
        transform: translateY(0px);
        opacity: 1 !important;
    }
</style>