<script>
  import Avatar from "./Avatar.svelte";
  import SocialLinks from "./SocialLinks.svelte";
</script>

<div class="about-container">
  <Avatar />
  <div class="about-text-container">
    <h1 class="about-title">Hi, I'm Oleksii Luchnikov</h1>
    <h2 class="about-short">Oil Painter, Digital Artist and Software Developer 
    <br />
    from Kharkiv, Ukraine.
    </h2>
    <p class="about-long" />
    <SocialLinks />
  </div>
</div>

<style>
  .about-container {
    font-family: "Fixel";
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 100%;
    transform: translateY(-5rem);
  }
  .about-text-container {
    margin: auto;
    margin-top: 1rem;
    margin-bottom: 1rem;
    max-width: 40%;
    padding: 0;
  }
  .about-title {
    font-size: 1.8rem;
    text-align: left;
    margin: 0;
    padding: 0;
  }
  .about-short {
    font-size: 1.2rem;
    font-weight: normal;
    text-align: flex-start;
    margin: 0;
    padding: 0;
  }
  .about-long {
    font-size: 1rem;
    text-align: left;
    padding: 0;
    margin-top: 0.5rem;
    margin-bottom: 1rem;
  }
</style>
