<script lang="ts">
    import yuhAudio from '../assets/sounds/yuh.mp3'
    import sadbAudio from '../assets/sounds/sad-b.mp3'
    import iWantItIGotItAudio from '../assets/sounds/i-want-it-i-got-it.mp3'
    import hiAudio from '../assets/sounds/hi.mp3'
    import fisherYatesFunc from '../utils/fisher-yates.func';

    let audioPlayer: HTMLAudioElement;
    let sounds = [
        yuhAudio,
        sadbAudio,
        iWantItIGotItAudio,
        hiAudio
    ];
    let counter = 0;

    const playRandomSound = () => {
        if (!audioPlayer) {
            return;
        }
        audioPlayer.src = handleArrayAccess();
        audioPlayer.play();
    }

    const handleArrayAccess: () => string = () => {
        const audio = sounds[counter];
        ++counter;
        
        if(counter >= sounds.length) {
            fisherYatesFunc(sounds);
            counter = 0;
        }

        return audio;
    }
</script>

<button on:click={playRandomSound}>
    Let's slay, darling
</button>

<audio bind:this={audioPlayer}
       id="dont-please"
       preload="auto"
></audio>
