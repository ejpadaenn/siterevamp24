<script>
    import Navbar from '$lib/components/Navbar.svelte'
</script>

<html lang="en">
    <Navbar />

    <div class="gencontainer">
        <h1 id="title1">Find a Church</h1>
        <div class="cardcontainer">
            <a href="/churches/nz"><div class="card"><h2>NZ</h2></div></a>
            <a href="/churches/aus"><div class="card"><h2>AUS</h2></div></a>
            <a href="/churches/asia"><div class="card"><h2>ASIA</h2></div></a>
            <a href="/churches/america"><div class="card"><h2>AMERICA</h2></div></a>
            <a href="/churches/europe"> <div class="card"><h2>EUROPE</h2></div></a>
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
        height: 120vh;
        max-width: 1920px;
    }

    .gencontainer {
        display: grid;
        grid-template-columns: 5% 1fr 5%;
        grid-template-rows: 20vh 1fr;

        margin-top: 20vh;
    }

    #title1 {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 1;
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

        display: flex;

        align-items: top;
        justify-content: left;
        padding-left: 1rem;
    }

    .card:hover {
        transition: all ease-out 0.25s;
        background-color: #dbdbdb;
    }

    .card:hover > h2 {
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
        color: #f7f7f7;
        letter-spacing: 0.1rem;
    }
</style>