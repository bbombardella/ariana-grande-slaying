<script lang="ts">
    import yuhAudio from '../assets/sounds/yuh.mp3'

    let audioPlayer: HTMLAudioElement;

    const sounds = [yuhAudio];
    const playRandomSound = () => {
        if (!audioPlayer) {
            return;
        }
        audioPlayer.src = sounds[Math.floor(Math.random() * sounds.length)];
        audioPlayer.play();
    }
</script>

<button on:click={playRandomSound}>
    Let's slay, darling
</button>

<audio bind:this={audioPlayer} id="dont-please"></audio>
