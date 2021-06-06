<svelte:options tag="docure-article" />

<script>
  export let title = '';
</script>

<div class="docure-article-title">
  {title}
</div>
<div class="docure-article-content">
  <slot />
</div>

<style>
  :host {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 20px 40px;
  }

  :host .docure-article-title {
    width: 100%;
    font-weight: bold;
    font-size: 18px;
  }

  :host .docure-article-content {
    width: 100%;
    margin-top: 20px;
  }
</style>
