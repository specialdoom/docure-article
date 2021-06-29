<svelte:options tag="docure-article" />

<script>
  export let title = '';
  export let workflow = '';
</script>

<div class="docure-article-title">
  {title}
  {#if workflow}
    <div class="docure-article-workflow">
      <a
        href={`http://localhost:4200/preview-workflow/${workflow}`}
        target="_blank"
      >
        Related workflow
      </a>
    </div>
  {/if}
</div>
<div class="docure-article-content">
  <slot />
</div>

<style>
  :host {
    position: relative;
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
    white-space: pre-wrap;
  }

  :host .docure-article-workflow {
    position: absolute;
    right: 20px;
    top: 15px;
    width: auto;
  }

  a {
    background-color: red;
    box-shadow: 0 5px 0 darkred;
    font-size: 12px;
    color: white;
    padding: 10px 10px;
    position: relative;
    text-decoration: none;
    text-transform: uppercase;
  }

  a:hover {
    background-color: #ce0606;
    cursor: pointer;
  }

  a:active {
    box-shadow: none;
    top: 5px;
  }
</style>
