<script>
    import Landing from '$lib/pagelib/homepage/Landing.svelte';

    import Invitation from '$lib/pagelib/homepage/Invitation.svelte';

    import Announcements from '$lib/pagelib/homepage/Announcements.svelte'

    import Footer from '$lib/components/Footer.svelte'
</script>

<Landing />

<Invitation/>

<Announcements/>

<Footer/>

<style>
    :global(html) {
        scroll-behavior: smooth;
    }

    :global(body) {
        margin: 0%;
    }
</style>