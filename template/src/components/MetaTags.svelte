<script lang="ts">
  export let url: string;
  export let title: string;
  export let description: string;
  export let keywords: string;
</script>

<svelte:head>
  <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
  <title>{title}</title>

  <meta name="theme-color" content="#0000" />
  <meta name="default-theme" content="auto" />
  <meta name="author" content="Svelte SSR Template" />
  <meta name="description" content={description} />
  <meta name="keywords" content="svelte-ssr-template,{keywords}" />
  <meta name="referrer" content="no-referrer" />

  <meta property="og:title" content={title} />
  <meta property="og:url" content={url.indexOf("https://") == 0 ? url : "https://example.com" + (url[0] == "/" ? url : "/" + url)} />
  <meta property="og:type" content="object" />
  <meta property="og:image" content="https://example.com/logo.png" />
  <meta property="og:site_name" content="Svelte SSR Template" />

  <link rel="icon" type="image/svg+xml" href="/logo.svg" />
  <link rel="icon" type="image/png" href="/logo.png" />
</svelte:head>
