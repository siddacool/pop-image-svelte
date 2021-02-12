<script>
  import Paper from './Paper.svelte';
</script>

<div class="tag-search">
  <Paper
    ><input
      type="text"
      name="tag-search-input"
      placeholder="Search tags e.g. sky, night"
    /></Paper
  >
</div>

<style type="text/scss">
  @import '../styles/mixins';

  .tag-search {
    border-radius: inherit;
    height: var(--unit-5);

    @include onDesktop {
      width: 400px;
    }

    :global(.paper) {
      height: 100%;
    }

    input {
      height: 100%;
      width: 100%;
      border: none;
      border-radius: inherit;
      margin: 0;
      padding: 0 var(--unit-2);
      display: flex;
      font-size: inherit;
      color: var(--color-grey-100);
      background-color: transparent;
      padding-top: 3px;

      &:focus {
        outline: none;
      }
    }
  }
</style>
