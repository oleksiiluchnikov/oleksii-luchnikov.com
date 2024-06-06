<script>
    import { onMount } from "svelte";

    /** @type {{ src: string }} */
    let avatar = {
        src: "",
    };

    /** Fetch avatar from GitHub
     * @param {string} src
     * @returns {Promise<string>}
     */
    async function fetchAvatar(src) {
        const res = await fetch(src);
        const blob = await res.blob();
        return URL.createObjectURL(blob);
    }

    onMount(async () => {
        avatar.src = await fetchAvatar(
            "https://avatars.githubusercontent.com/u/40718392?v=4"
        );
    });
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
