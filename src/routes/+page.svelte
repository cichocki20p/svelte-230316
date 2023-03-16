<script>
    import Nav from "../components/nav.svelte";
    import { count } from '../components/stores.js';
    import ActionButtons from '../components/stores-actions.svelte';

    let countValue;

    count.subscribe(value => {
        countValue = value;
    });
</script>

<h1>This is <i>Home</i> Page</h1>
<Nav/>
<p>The count is {countValue}</p>
<ActionButtons/>