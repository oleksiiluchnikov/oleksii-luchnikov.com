<script>
    import "../app.css";
    import About from "../components/About.svelte";
    import Footer from "../components/Footer.svelte";
    import {  onMount } from "svelte";
    // TODO: Implement Menu component
    // import Menu from "../components/Menu.svelte";

    /** Path to the background image */
    const background = "/background.jpg";

    /** @type {HTMLDivElement} Reference to the container div element */
    let containerDiv;

    /**
     * Sets up the background image with lazy loading support
     * Handles both modern browsers with native lazy loading and provides fallback
     */
    onMount(() => {
        if ('loading' in HTMLImageElement.prototype) {
            containerDiv.style.backgroundImage = `url(${background})`;
        } else {
            // Fallback for browsers that don't support lazy loading
            const img = new Image();
            img.src = background;
            img.onload = () => {
                containerDiv.style.backgroundImage = `url(${background})`;
            };
        }
    });

</script>

<!-- <div class="main-container" style="background-image: url({background});"> -->
<div bind:this={containerDiv} class="main-container">
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
