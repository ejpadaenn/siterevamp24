<script>
    import Navbar from '$lib/components/Navbar.svelte'
</script>

<html lang="en">
    <Navbar />

    <div class="landingcontainer">
        <h1 id="title1">Who Are We</h1>

        <h2 class="subtitle">We are non-sectarian, non-denominational, evangelistic and missionary-sending church.
        Proclaiming salvation, healing, deliverance and the coming of our Lord Jesus Christ.</h2>

        <div class="para">
            <p>We believe in One God in Three Distinct Persons. We believe in JESUS CHRIST our Saviour who came to us by virgin birth.
            We believe that He died to save us, bore our sins, was crucified, then from death He rose again victorious and ascended to the Father's side.
            We believe in the Holy Spirit sent by God to His church with gifts and power.</p>
        
            <p>Our mission is to encourage everyone to build a strong relationship with our Lord Jesus Christ,
            and to motivate every believer to grow and participate in fulfilling their calling and purpose in the Lord.</p>
        </div>
    </div>
</html>
<!--add muted image of the church as a background-->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">

<style>
    /**hides the scrollbar*/
    html::-webkit-scrollbar {
        display: none;
    }

    html {
        height: 90vh;
        max-width: 1920px;
    }

    .landingcontainer {
        display: grid;
        grid-template-columns: 5% 1fr 50%;
        grid-template-rows: 20vh 1fr 1fr;
    }

    #title1 {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 2;
    }

    .subtitle {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 3;
    }

    .para {
        color: #252626;
        grid-column: 2 / 3;
        grid-row: 4
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
        font-weight: 500;
        font-style: normal;
        font-size: 1.4rem;
    }

    p {
        font-family: "Poppins", sans-serif;
        font-weight: 500;
        font-style: normal;
    }
</style>