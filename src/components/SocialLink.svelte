<script>
export let name, url, icon, label;
// check if icon file exist
const iconFile = `/icons/${icon}.svg`;
let isIconExists = false;

const icons = import.meta.glob('/public/icons/*.svg', { eager: true });
isIconExists = !!icons[iconFile];
</script>

<li class="social-link">
    <a href={url} target="_blank" rel="noopener noreferrer" aria-label={label}>
        {#if icon && isIconExists}
            <svg class="social-link-icon" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true" role="img">
                <use xlink:href={`/icons/${icon}.svg#icon`} />
            </svg>
        {/if}
        <span class="social-link-name">{name}</span>
    </a>
</li>

<style>
.social-link a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: #fff;
    font-size: 1rem;
    border-radius: 0.4rem;
    background-color: var(--bg-primary);
    padding: 0.4rem 1rem;
    position: relative;
    transition: transform 0.2s ease, box-shadow 0.2s ease
}

.social-link a:focus-visible {
    outline: 3px solid #fff;
    outline-offset: 2px;
}

.social-link a:hover,
.social-link a:focus {
    box-shadow: 5px 5px 0px rgba(0, 0, 0, 1);
    transform: translateX(-5px) translateY(-5px);
}

.social-link a:focus:not(:focus-visible) {
    outline: none;
}

@media (prefers-reduced-motion: reduce) {
    .social-link a {
        transition: none;
    }
}

.social-link-name {
    font-size: 1rem;
}
</style>
