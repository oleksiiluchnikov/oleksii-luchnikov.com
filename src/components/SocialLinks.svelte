<script>
import SocialLink from './SocialLink.svelte';

const socialLinks = [
    {
        name: 'ArtStation',
        url: 'https://www.artstation.com/luchnikov',
        icon: 'artstation',
        label: 'View my artwork on ArtStation'
    },
    {
        name: 'Instagram',
        url: 'https://www.instagram.com/oleksii_luchnikov/',
        icon: 'instagram',
        label: 'Follow me on Instagram'
    },
    {
        name: 'Twitter',
        url: 'https://twitter.com/o_luchnikov',
        icon: 'twitter',
        label: 'Follow me on Twitter'
    },
    {
        name: 'GitHub',
        url: 'https://github.com/oleksiiluchnikov',
        icon: 'github',
        label: 'Check my code on GitHub'
    },
    {
        name: 'Facebook',
        url: 'https://www.facebook.com/oleksiiluchnikov',
        icon: 'facebook',
        label: 'Connect with me on Facebook'
    },
    {
        name: 'LinkedIn',
        url: 'https://www.linkedin.com/in/oleksii-luchnikov/',
        icon: 'linkedin',
        label: 'Connect with me on LinkedIn'
    },
];

</script>

<nav aria-label="Social media profiles" class="social-navigation">
    <h2 class="visually-hidden">Connect with me on social media</h2>
    <ul class="social-links-container" role="list">
        {#each socialLinks as {name, url, icon, label}}
            <SocialLink {name} {url} {icon} {label} />
        {/each}
    </ul>
</nav>

<style>
    .social-navigation {
        display: flex;
        align-items: left;
        margin: 1.5rem 0;
    }

    .social-links-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 1rem;
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .visually-hidden {
        position: absolute;
        width: 1px;
        height: 1px;
        padding: 0;
        margin: -1px;
        overflow: hidden;
        clip: rect(0, 0, 0, 0);
        white-space: nowrap;
        border: 0;
    }

    @media (max-width: 480px) {
        .social-links-container {
            gap: 0.75rem;
        }
    }
</style>
