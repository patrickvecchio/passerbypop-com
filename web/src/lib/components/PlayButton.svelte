<script lang="ts">
    import { Play, Pause } from '@lucide/svelte';

    let {
        size,
        fill
    }: {
        size: number;
        fill: string;
    } = $props();

    let isPaused = $state(true);
    let audioFile = {} as HTMLMediaElement;

    const togglePlay = () => {
        isPaused = !isPaused;
        if (isPaused) {
            audioFile.pause();
        } else {
            audioFile.play();
        }
    };

    const onEnded = () => {
        isPaused = true;
    };
</script>

<audio
    bind:this={audioFile}
    src="audio/downbeat-example-2.wav"
    onended={onEnded}
></audio>

<button type="button" class="btn-icon preset-filled" title="Play/Pause" onclick={togglePlay}>
    {#if isPaused}
        <Play size={size} fill={fill} />
    {:else  }
        <Pause size={size} fill={fill} />
    {/if}
</button>