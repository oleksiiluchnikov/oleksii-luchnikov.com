<script>
    import { page } from '$app/stores';
    $: currentPath = $page.url.pathname;
</script>

<nav aria-label="Main navigation">
    <ul class="menu-container" role="menubar">
        <li class="menu-item" role="none">
            <a href="/" role="menuitem" aria-current={currentPath === '/' ? 'page' : undefined}>Home</a>
        </li>
        <li class="menu-item" role="none">
            <a href="/art" role="menuitem" aria-current={currentPath === '/art' ? 'page' : undefined}>Art</a>
        </li>
        <li class="menu-item" role="none">
            <a href="/code" role="menuitem" aria-current={currentPath === '/code' ? 'page' : undefined}>Code</a>
        </li>
        <li class="menu-item" role="none">
            <a href="/about" role="menuitem" aria-current={currentPath === '/about' ? 'page' : undefined}>About</a>
        </li>
        <li class="menu-item" role="none">
            <a href="/contact" role="menuitem" aria-current={currentPath === '/contact' ? 'page' : undefined}>Contact</a>
        </li>
    </ul>
</nav>

<style>
.menu-container {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    gap: 1rem;
    list-style: none;
    padding: 0;
    margin: 0;
}

.menu-item {
    list-style: none;
    border-radius: 0.4rem;
    padding: 0.4rem;
    background-color: #13123d;
}

.menu-item a {
    text-decoration: none;
    color: #fff;
    padding: 0.4rem;
    display: inline-block;
}

.menu-item a:hover,
.menu-item a:focus {
    text-decoration: underline;
    outline: 2px solid #fff;
    outline-offset: -2px;
}

.menu-item a[aria-current="page"] {
    font-weight: bold;
    text-decoration: underline;
}
</style>
