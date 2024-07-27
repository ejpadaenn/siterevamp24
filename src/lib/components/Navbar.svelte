<script>
    import favicon from '$lib/components/favicon.png'
</script>

<div class="navbar">
    <img src="{favicon}" alt="logo" class="navlogo">
    <nav class="links">
        <a href="/">Home</a>
        <a href="/about">About Us</a>
        <a href="/churches">Churches</a>
        <a href="#contact">Contact Us</a>
    </nav>
</div>

<style>

    .navbar {
        height: 5rem;
        width: 100%;
        margin: 0;

        background-color: white;

        position: fixed;
        left: 0;
        top: 0;

        display: flex;
        align-items: center;

        z-index: 10;
    }

    .navlogo {
        max-width: 3rem;
        max-height: 3rem;
        margin-left: 5.5rem;
    }

    a {
        font-family: "Poppins", sans-serif;
        font-weight: 600;
        font-style: normal;
        font-size: 1.5rem;
        text-decoration: none;

        padding: 1.5rem;

        color: #252626;
    }

    .links {
        margin-left: 45%;
    }
</style>