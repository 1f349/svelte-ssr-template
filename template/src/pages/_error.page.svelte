<script lang="ts">
  import {navigate} from "vite-plugin-ssr/client/router";
  import MetaTags from "~/components/MetaTags.svelte";
  import Layout from "./__layout.svelte";

  export let __;
  export let pageProps;
</script>

<MetaTags url={__.urlOriginal} title="Error" description="" keywords="error,error page" />

<Layout>
  <div>
    {#if pageProps.is404}
      <h1 class="title-text">404 Not Found</h1>
      <p class="coming-soon">You have lost your way, please return to valid paths.</p>
      <p><button on:click={() => navigate("/")} class="refresh-btn">Back to homepage</button></p>
    {:else}
      <h1 class="title-text">500 Internal Server Error</h1>
      <p class="coming-soon">The server had an issue with this page.</p>
      <p><button on:click={() => navigate("/")} class="refresh-btn">Back to homepage</button></p>
    {/if}
  </div>
</Layout>
