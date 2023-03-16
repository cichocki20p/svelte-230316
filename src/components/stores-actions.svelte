<script>
    import Page from '../routes/+page.svelte';
    import { count } from './stores.js';

    function increment() {
        count.update(val => val + 1);
    }

    function decrement() {
        count.update(val => val - 1);
    }

    function reset() {
        count.set(111);
    }
</script>

<div>
    <input type="button" on:click={increment} value="+ 1">
    <input type="button" on:click={decrement} value="- 1">
    <input type="button" on:click={reset} value="reset">
</div>

<style>
    div {
        border: 2px dotted #ddd;
        margin: 5px;
        padding: 5px;
    }
</style>