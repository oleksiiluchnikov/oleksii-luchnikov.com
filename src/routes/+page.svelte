<script>
    import "../app.css";
    import About from "../components/About.svelte";
    import Footer from "../components/Footer.svelte";

    let background = "/background.jpg";
</script>

<div class="main-container" style="background-image: url({background})">
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
        background: url("https://cdna.artstation.com/p/assets/images/images/005/091/416/large/oleksij-luchnikov-outskirts-luchnikov.jpg?1488394227");
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
    }
</style>
