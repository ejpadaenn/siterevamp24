<html lang="en">
    <div class="footerwrap" id="contact">
        <h1 class="maintext">Contact us!</h1>
        <div class="mailwrap">
            <h2>Mailing Address</h2>
            <h3>8 Mountwell Crescent, Auckland, New Zealand.</h3>
            <h3 class="balance">Please address all communication to the 'CNCI Admin'.</h3>
        </div>
        <div class="emailwrap">
            <h2>Phone and Email</h2>
            <h3>+64 021 241 1208</h3>
            <h3 class="email">JENNIFERU.CNCI@gmail.com</h3>
        </div>
    </div>

    <script src="src/lib/scrollreveal.js"></script>
</html>

<style>
    html {
        height: 50vh;
        min-height: 20vh;
        max-height: 50vh;
        width: 100vw;
        max-width: 100vw;

        background-color: #252626;


    }

    .footerwrap {
        height: 50vh;
        
        display: grid;
        grid-template-columns: 5% 1fr 1fr 5%;
        grid-template-rows: 10vh 1fr;
    }

    .mailwrap {
        grid-column: 2 / 3;
        grid-row: 2;
        justify-self: center;
    }

    .emailwrap {
        grid-column: 3 / 4;
        grid-row: 2;
        justify-self: center;
    }

    .mailwrap, .emailwrap {
        margin-top: 5vh;
    }
    
    .email {
        margin-top: 1rem;
    }

    .balance {
        margin-top: 1rem;
    }

    h1 {
        grid-column: 2 / 4;
        grid-row: 1 / 2;

        align-self: end;
        justify-self: center;

        font-family: "Poppins", sans-serif;
        font-weight: 700;
        font-style: normal;
        font-size: 3rem;

        line-height: 6rem;
        margin-bottom: 0;

        color: white;
    }

    h2 {
        font-family: "Poppins", sans-serif;
        font-weight: 500;
        font-style: normal;
        font-size: 1.75rem;

        margin-bottom: 0;

        color: white;
    }

    h3 {
        font-family: "Poppins", sans-serif;
        font-weight: 300;
        font-style: normal;
        font-size: 1.1rem;

        margin-top: 5vh;
        margin-bottom: 0;

        color: white;
    }

    .reveal {
        position: relative;
        transform: translateY(50px);
        opacity: 0;

        transition: all 1s ease;
    }
</style>