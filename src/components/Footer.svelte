<footer>
  <p class="footer-text">
    © {new Date().getFullYear()} <a href="/" aria-label="Homepage">Oleksii Luchnikov</a>.
  </p>
</footer>

<style>
  footer {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 1.2em;
    opacity: 0.5;
    background-color: transparent;
    padding: 0.3rem 0;
    margin-top: auto;
  }

  .footer-text {
    font-size: 0.8em;
    text-align: center;
    width: 100%;
    margin: 0;
  }

  .footer-text a {
    color: var(--text-normal);
    font-weight: normal;
    text-decoration: none;
    transition: opacity 0.2s ease;
  }

  .footer-text a:hover,
  .footer-text a:focus {
    opacity: 0.8;
    text-decoration: underline;
  }

  .footer-text a:focus-visible {
    outline: 2px solid var(--text-normal);
    outline-offset: 2px;
  }
</style>
