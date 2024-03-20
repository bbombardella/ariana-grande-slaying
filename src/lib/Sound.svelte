<script lang="ts">
    import yuhAudio from '../assets/sounds/yuh.mp3'
    import sadbAudio from '../assets/sounds/sad-b.mp3'
    import iWantItIGotItAudio from '../assets/sounds/i-want-it-i-got-it.mp3'
    import hiAudio from '../assets/sounds/hi.mp3'

    let audioPlayer: HTMLAudioElement;

    const sounds = [
        yuhAudio,
        sadbAudio,
        iWantItIGotItAudio,
        hiAudio
    ];
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

<audio bind:this={audioPlayer}
       id="dont-please"
       preload="auto"
></audio>
