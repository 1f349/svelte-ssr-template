<script lang="ts">
  import MetaTags from "~/components/MetaTags.svelte";
  import Layout from "./__layout.svelte";

  export let __;
  export let pageProps;
</script>

<MetaTags url={__.urlOriginal} title="Svelte SSR Template" description="Svelte SSR Template Home Page" keywords="" />

<Layout isHome={true}>
  <h1 class="title-text">Svelte SSR Template</h1>
</Layout>

<style lang="scss">
  .title-text {
    margin: 0 0 24px 0;
    font-size: 3.2em;
    line-height: 1.1;
  }
</style>
