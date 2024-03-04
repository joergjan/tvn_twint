<script lang="ts">
    import { currentPage } from "$lib/stores";
    import { onMount } from "svelte";

    let paymentAmount: number;
</script>

<svelte:head>
    <title>TV Nussbaumen</title>
    <meta name="robots" content="noindex, nofollow" />
</svelte:head>

<h1>TWINT</h1>

<div class="flex flex-col items-center">
    <input
        type="number"
        placeholder="Betrag eingeben"
        bind:value={paymentAmount}
        pattern="[0-9]*"
        class="border-2 border-gray-300 p-2 mb-4 text-center"
    />
    <form action="?/pay">
        <input type="number" hidden bind:value={paymentAmount} />
    </form>
</div>
