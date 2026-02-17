<script lang="ts">
    import "../app.css";

    let { children } = $props();
</script>

<svelte:head>
    <link
        rel="stylesheet"
        href="https://raw.githubusercontent.com/sindresorhus/modern-normalize/refs/heads/main/modern-normalize.css"
    />
</svelte:head>

<nav style:border="solid red 1px">
    <h1>layout.svelte</h1>
</nav>
{@render children()}
