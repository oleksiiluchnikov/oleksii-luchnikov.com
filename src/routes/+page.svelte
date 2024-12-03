<script>
    import "../app.css";
    import About from "../components/About.svelte";
    import Footer from "../components/Footer.svelte";
    // TODO: Implement Menu component
    // import Menu from "../components/Menu.svelte";

    const background = "/background.jpg";
</script>

<div class="main-container" style="background-image: url({background});">
    <About />
</div>
<Footer />

<style>
    .main-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
    }
</style>
