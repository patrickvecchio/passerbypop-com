<script lang="ts">
	const wwwiigSource = 'https://www.youtube.com/embed/06a6pp3MsBI?si=qkrTyy0ys544-zDo';
	const passerbySource = 'https://www.youtube.com/embed/FaVT2aeTWCI?si=Z8duGU_XhcZYxaMu';

	let videoSource = wwwiigSource;
</script>

<div
	class="w-[600px] h-[516px] bg-[url('/images/3d-bucking-bronco-transparent.png')] bg-center bg-no-repeat align-center content-center"
>
	<iframe
		width="560"
		height="315"
		src={videoSource}
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
		referrerpolicy="strict-origin-when-cross-origin"
		allowfullscreen
	></iframe>

	<div class="flex justify-start mt-4 gap-4">
		<button type="button" on:click={() => (videoSource = wwwiigSource)}>
			<img src="/images/www-iig-video-thumbnail.png" alt="www,iig video thumbnail" />
		</button>
		<button type="button" on:click={() => (videoSource = passerbySource)}>
			<img src="/images/passerby-video-thumbnail.png" alt="Passerby video thumbnail" />
		</button>
	</div>
</div>
