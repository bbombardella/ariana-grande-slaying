<script lang="ts">
    import yuhAudio from '../assets/sounds/yuh.mp3'

    let audioPlayer: HTMLAudioElement;

    const sounds = [yuhAudio];
    const playRandomSound = async () => {
        if (!audioPlayer) {
            return;
        }
        await audioPlayer.play();
        audioPlayer.src = sounds[Math.floor(Math.random() * sounds.length)];
    }
</script>

<button on:click={playRandomSound}>
    Let's slay, darling
</button>

<audio bind:this={audioPlayer}
       id="dont-please"
       src={yuhAudio}
       preload="auto"
></audio>
