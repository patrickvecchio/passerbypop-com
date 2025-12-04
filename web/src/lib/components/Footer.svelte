<script lang="ts">
    import PlayButton from "$lib/components/PlayButton.svelte";

</script>

<div class="flex justify-between">
    <div>
        <div class="flex grow gap-2">
            <img class="" src="/images/passerby-thumbnail.jpg" alt="Passerby Album Cover" />
            <div class="">
                <div class="mb-2">An All New Romance</div>
                <div class="mb-2">
                    <PlayButton size={32} fill="white" />
                </div>
            </div>
        </div>
    </div>
    <div class="">
        <form class="block">
            <input
                type="email"
                placeholder="Your email"
                class="rounded-xl px-4 py-2"
            />
            <button
                type="submit"
                class="btn-icon preset-filled text-sm" title="Join"
            >
                Join
            </button>
        </form>
    </div>
</div>