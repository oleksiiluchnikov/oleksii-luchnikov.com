<script>
    import "../app.css";
    import About from "../components/About.svelte";
    import Footer from "../components/Footer.svelte";
    import Avatar from "../components/Avatar.svelte";
    import SocialLinks from "../components/SocialLinks.svelte";

    import {  onMount } from "svelte";
    // TODO: Implement Menu component
    // import Menu from "../components/Menu.svelte";

    /** Path to the background image */
    const background = "/background.webp";
    const background120 = "/background-120.webp";
    const background240 = "/background-240.webp";
    const background480 = "/background-480.webp";
    const background768 = "/background-768.webp";
    const background1920 = "/background-1920.webp";
    const background3840 = "/background-3840.webp";

    /** @type {HTMLDivElement} Reference to the container div element */
    let containerDiv;

    /**
     * Sets up the background image with lazy loading support
     * Handles both modern browsers with native lazy loading and provides fallback
     */
    onMount(() => {
        const setBackground = (src) => {
            containerDiv.style.backgroundImage = `url(${src})`;
        };

        // Start with smallest image for immediate display
        setBackground(background);

        // Load higher resolution images progressively
        const loadImage = (src) => {
            return new Promise((resolve, reject) => {
                const img = new Image();
                img.onload = () => {
                    setBackground(src);
                    resolve();
                };
                img.onerror = reject;
                img.src = src;
            });
        };

        // Progressive loading based on screen width
        const screenWidth = window.innerWidth;
        const loadSequence = async () => {
            if (screenWidth >= 120) await loadImage(background240);
            if (screenWidth >= 240) await loadImage(background120);
            if (screenWidth >= 480) await loadImage(background768);
            if (screenWidth >= 768) await loadImage(background1920);
            if (screenWidth >= 1920) await loadImage(background3840);
        };

        loadSequence();
    });

</script>

<div bind:this={containerDiv} class="main-container" role="main">
<section class="about-text-container">
    <Avatar />
    <About />
    <SocialLinks />
</section>
</div>
<Footer />

<style>
.main-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: left;
    height: 100%;
    margin: 0;
    background: #4542ca;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    transition: background-image 0.6s ease-in-out;
}
.about-text-container {
    display: flex;
    gap: 1rem;
    flex-direction: column;
    justify-content: center;
    align-items: left;
    max-width: 500px;
    font-family: "Fixel Display";
    margin: auto;
    margin-top: 1rem;
    margin-bottom: 1rem;
    padding: 0;
}
</style>
