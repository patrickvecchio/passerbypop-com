<script lang="ts">
	import { Portal, Popover, usePopover } from '@skeletonlabs/skeleton-svelte';
	const copyToClipboard = (text: string) => {
		navigator.clipboard.writeText(text);
	};

	const id = $props.id();
	const popover = usePopover({
		id: id,
		closeOnInteractOutside: false
	});

	function showAndHide() {
        copyToClipboard("info@passerbymusic.com");
		popover().setOpen(true);
		setTimeout(() => {
			popover().setOpen(false);
		}, 2000);
	}
</script>

<div
	class="w-[600px] h-[516px] bg-[url('/images/3d-bucking-bronco-transparent.png')] bg-center bg-no-repeat align-center content-center"
>
	<div class="flex flex-col justify-center-safe mt-0ml-0">
		<button type="button" onclick={() => showAndHide()}>
			<img src="/images/info@passerbymusic.com-in-3D.png" alt="info@passerbymusic.com" />
		</button>

		<Popover.Provider value={popover}>
			<Popover.Trigger class="btn"></Popover.Trigger>
			<Portal>
				<Popover.Positioner>
					<Popover.Content class="card max-w-sm p-4 bg-surface-100-900 shadow-xl space-y-2">
						<Popover.Description
							>Copied to clipboard</Popover.Description
						>
					</Popover.Content>
				</Popover.Positioner>
			</Portal>
		</Popover.Provider>
	</div>
</div>
