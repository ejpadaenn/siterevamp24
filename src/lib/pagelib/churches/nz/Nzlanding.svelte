<script>
    import Navbar from '$lib/components/Navbar.svelte'
</script>

<html lang="en">
    <Navbar />

    <div class="gencontainer">
        <h1 id="title1">NZ Churches</h1>
        <div class="cardcontainer">
            <a href="/churches/nz/hq"><div class="card"><h2>Auckland HQ</h2></div></a>
            <a href="/churches/nz/cbd"><div class="card"><h2>Auckland CBD</h2></div></a>
            <a href="/churches/nz/west"><div class="card"><h2>Auckland West</h2></div></a>
            <a href="/churches/nz/south"><div class="card"><h2>Auckland South</h2></div></a>
            <a href="/churches/nz/northshore"><div class="card"><h2>Auckland North Shore</h2></div></a>
            <a href="/churches/nz/whangarei"><div class="card"><h2>Whangarei</h2></div></a>
            <a href="/churches/nz/hamilton"><div class="card"><h2>Hamilton</h2></div></a>
            <a href="/churches/nz/cambridge"><div class="card"><h2>Cambridge</h2></div></a>
            <a href="/churches/nz/tokoroa"><div class="card"><h2>Tokoroa</h2></div></a>
            <a href="/churches/nz/rotorua"><div class="card"><h2>Rotorua</h2></div></a>
            <a href="/churches/nz/gisborne"><div class="card"><h2>Gisborne</h2></div></a>
            <a href="/churches/nz/tauranga"><div class="card"><h2>Tauranga</h2></div></a>
            <a href="/churches/nz/wellington"><div class="card"><h2>Wellington</h2></div></a>
            <a href="/churches/nz/christchurch"><div class="card"><h2>Christchurch</h2></div></a>
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
        height: 210vh;
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