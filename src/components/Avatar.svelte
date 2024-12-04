<script>
    /** @type {{ src: string }} */
    let avatar = {
        src: "/avatar.webp"
    };

</script>

<div class="avatar-container">
    <img class="avatar" src={avatar.src} alt="avatar" />
</div>

<style>
    .avatar-container {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .avatar {
        width: 10rem;
        height: 10rem;
        border-radius: 1rem;
    }
</style>
