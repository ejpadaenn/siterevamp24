<script>
    import Navbar from '$lib/components/Navbar.svelte'

    import { onMount } from 'svelte'

    onMount(() => {
        console.log('attaching scrollreveal js');
        const config = document.createElement('script');
        config.src = '$lib/scrollreveal.js'; // might be outdated so check for an update can link
        config.async= true;
        document.body.appendChild(config);
    });
</script>

<html lang="en">
    <Navbar />

    <div class="landcontainer">
        <h1 id="title1">Melbourne</h1>
        <h2 id="sub1">Sunday 2:30pm</h2>
        <p>Sunday services are held in the afternoon to cater those who want to attend from Melbourne.
        The church is currently using the Saltwater Community Centre as a venue.</p>
    </div>

    <div class="servicecontainer">
        <h2 id="title2" class="reveal">Services</h2>
        <div class="cardcontainer reveal">
            <a href="https://maps.app.goo.gl/xGkegxRmeYdy1eVv7" target="_blank"><div class="card">
                <h2 class="cardtitle">2:30pm Service</h2>
                <div class="cardtextcon">
                    <p class="cardtext">Every Sunday</p>
                    <p class="cardtext">Saltwater Community Centre, 153 Saltwater Promenade</p>
                </div>
            </div></a>
        </div>
    </div>
</html>
<!--add background of world-->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">

<style>
    /**hides the scrollbar*/
    html::-webkit-scrollbar {
        display: none;
    }

    html {
        height: 180vh;
        max-width: 1920px;
    }

    .landcontainer {
        display: grid;
        grid-template-columns: 5vw 1fr 1fr 5vw;
        grid-template-rows: 10vh 1fr 1fr 20vh;
    }

    .servicecontainer {
        width: 100vw;
        max-width: 1920px;
        height: 100vh;
        display: grid;
        grid-template-columns: 5% 1fr 5%;
        grid-template-rows: 20vh 1fr;

        margin-top: 20vh;

        background-color: #708fb8;
    }

    #title1 {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 3;
    }

    #title2 {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 1;
        align-self: end;

        font-weight: 500;
        font-size: 3rem;
    }

    #sub1 {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 4;
    }

    p {
        font-family: "Poppins", sans-serif;
        font-weight: 300;
        font-style: normal;
        font-size: 1rem;
        margin-bottom: 0;

        color: #252626;
        grid-column: 2 / 3;
        grid-row: 4;

        align-self: center;
    }

    .cardcontainer {
        grid-column: 2 / 3;
        grid-row: 2;

        display: flex;
        flex-wrap: wrap;
        gap: 1.5rem;

        justify-content: center;

        margin-top: 10vh;
    }
    
    .card {
        width: 25vw;
        height: 30vh;
        background-color: #404040;

        display: grid;
        grid-template-columns: 1vw 1fr 1fr 1vw;
        grid-template-rows: 1vh 1fr 1fr 1vh;
    }

    .cardtitle {
        grid-column: 2 / 3;
        grid-row: 1 / 3;

        justify-self: start;

        line-height: 2rem;
    }

    .cardtextcon {
        grid-column: 2 / 3;
        grid-row: 3 / 4;
        
        align-self: center;
    }

    .cardtext {
        color: #708fb8;
        line-height: 1rem;
    }

    .card:hover {
        transition: all ease-out 0.25s;
        background-color: #dbdbdb;
    }

    .card:hover > h2 {
        transition: all ease-out 0.2s;
        color: #404040;
    }

    .card:hover > .cardtextcon > p {
        transition: all ease-out 0.2s;
        color: #404040;
    }

    a {
        text-decoration: none;
    }

    h1 {
        font-family: "Poppins", sans-serif;
        font-weight: 700;
        font-style: normal;
        font-size: 5rem;
        line-height: 6rem;
        margin-bottom: 0;
    }

    h2 {
        font-family: "Poppins", sans-serif;
        font-weight: 300;
        font-style: normal;
        font-size: 2rem;
        line-height: 1rem;
        color: #708fb8;
        letter-spacing: 0.1rem;
    }

    .reveal {
        position: relative;
        transform: translateY(50px);
        opacity: 0;

        transition: all 1s ease;
    }
</style>