<script lang="ts">
    import Ariana from './lib/Ariana.svelte';
    import Sound from './lib/Sound.svelte'
</script>

<main>
    <h1>Slay, Ariana 💅</h1>
    <Sound />
    <Ariana/>
</main>

<style>
    main {
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
    }
</style>
