<script lang="ts">
    import arianaImage from '../assets/ariana.webp'
</script>

<img src={arianaImage} class="ariana" alt="Ariana Grande"/>

<style>
    .ariana {
        flex: 1;
        max-width: 100%;
        aspect-ratio: 6 / 1;
        margin: 0 1em;
        object-fit: contain;
        object-position: bottom;
        will-change: filter;
        transition: filter 300ms;
    }

    .ariana:hover {
        filter: drop-shadow(0 0 2em #ff3e00aa);
    }
</style>
