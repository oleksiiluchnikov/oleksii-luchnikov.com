<script>
const name = "Oleksii Luchnikov";
const short = "oil painter / key frame illustrator / concept artist for Films, Commercials & more";
const from = "Kharkiv, Ukraine";
</script>
<div class="text-container">
    <h1 class="about-title">Hi, I'm <strong>{name}</strong></h1>
    <h2 class="about-short">{short}
        <br aria-hidden="true" />
        from {from}
    </h2>
</div>
<style>

.text-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: left;
    gap: 0;
}
.about-title {
    font-weight: 500;
    font-size: 1.8rem;
    text-align: left;
    margin: 0;
}

.about-title strong {
    font-family: "Fixel Display";
    font-weight: 900;
}
.about-short {
    font-size: 1rem;
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
