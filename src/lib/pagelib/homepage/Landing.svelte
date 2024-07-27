<script>
    import Navbar from '$lib/components/Navbar.svelte'
</script>

<html lang="en">
    <Navbar />

    <div class="landingcontainer">
        <div class="landingtext">
            <h1>Christ New Creation International</h1>
            <p class="verse1">“You are the Lord, you alone. You have made heaven, the heaven of heavens,
                with all their host, the earth and all that is on it, the seas and all that is in them;
                and you preserve all of them; and the host of heaven worships you."</p>
            <p class="verse1ref">Nehemiah 9:6</p>
        </div>
        <video autoplay loop muted plays-inline id="bgvideo" preload="none">
            <source src="assets/homepage/bg19201080clouds.mp4" type="video/mp4" />
        </video>
    </div>  
    
</html>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">


<style>
    /**hides the scrollbar*/
    html::-webkit-scrollbar {
        display: none;
    }

    html {
        height: 100vh;
        max-width: 1920px;
    }
    
    .landingcontainer {
        display: grid;
        grid-template-columns: 5% 1fr 5%;
        grid-template-rows: 60% 1fr;
    }

    .landingtext {
        height: 50%;
        width: 60%;

        grid-column: 2 / 3;
        grid-row: 2;

        color: white;
    }
    
    .verse1 {
        font-size: 1.2rem;
        margin-bottom: 0;
    }

    .verse1ref {
        font-size: 1rem;
    }

    h1 {
        font-family: "Poppins", sans-serif;
        font-weight: 700;
        font-style: normal;
        font-size: 5rem;
        line-height: 6rem;
        margin-bottom: 0;
    }

    p {
        font-family: "Poppins", sans-serif;
        font-weight: 500;
        font-style: normal;
    }

    /**coding for background video*/
    #bgvideo {
        position: absolute;
        top: 0;
        left: 0;

        z-index: -1;
        
        clip-path: inset(0 0 0 0);
        object-fit: cover;
        filter: brightness(90%);
    }

    @media (min-aspect-ratio: 16/9){
        #bgvideo{
            width: 100%;
            height: auto;
        }
    }

    @media (max-aspect-ratio: 16/9){
        #bgvideo{
            width: auto;
            height: 100%;
        }
    }
</style>