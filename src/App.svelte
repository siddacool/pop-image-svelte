<script>
  import TagSearch from './components/TagSearch.svelte';
</script>

<div class="App">
  <header class="sidePadding"><TagSearch /></header>
  <main>main</main>
  <nav>nav</nav>
</div>

<style type="text/scss">
  @import './styles/mixins';

  :global(:root) {
    --unit-1\4: 2px;
    --unit-1\2: 4px;
    --unit-1: 8px;
    --unit-2: 16px;
    --unit-3: 24px;
    --unit-4: 32px;
    --unit-5: 40px;
    --unit-6: 48px;
    --unit-7: 56px;
    --unit-8: 64px;
    --unit-9: 72px;
    --unit-10: 80px;

    --border-radius-1\2: 2px;
    --border-radius-1: 4px;
    --border-radius-2: 6px;
    --border-radius-3: 8px;

    // colors
    --color-white: #fff;
    --color-grey-10: #f5f5f5;
    --color-grey-100: #1d1d1d;

    // const colors
    --color-const-white: var(--color-white);

    // extra
    --side-padding-padding: var(--unit-2);
  }

  :global(.dark) {
    --color-white: #000;
    --color-grey-10: #504f4f;
    --color-grey-100: #f3f3f3;
  }

  :global(.App) {
    font-family: 'Rubik', sans-serif;
    min-height: inherit;
    padding-top: var(--unit-3);
    font-size: 16px;
    background-color: var(--color-grey-10);
  }

  :global(.sidePadding) {
    padding: 0 var(--side-padding-padding);

    @include onTablet {
      --side-padding-padding: var(--unit-3);
    }
  }
</style>
