<script lang="ts">
	const goHome = () => {
		window.location.href = '/';
	};
</script>

{#snippet facebook(size: number, fill: string)}
	<svg
		width={size}
		height={size}
		viewBox="0 0 24 24"
		fill="none"
		xmlns="http://www.w3.org/2000/svg"
	>
		<path
			d="M22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.0228 5.65685 21.1599 10.4375 21.9102V14.9219H7.89844V12H10.4375V9.79688C10.4375 7.28906 11.9307 5.90625 14.2158 5.90625C15.3087 5.90625 16.4531 6.10195 16.4531 6.10195V8.59375H15.1921C13.9492 8.59375 13.5625 9.33582 13.5625 10.0977V12H16.3359L15.8926 14.8906H13.5625V21.9102C18.3431 21.1599 22 17.0228 22 12Z"
			{fill}
		/>
	</svg>
{/snippet}

{#snippet youtube(size: number, fill: string)}
	<svg
		width={size}
		height={size}
		viewBox="0 0 24 24"
		fill="none"
		xmlns="http://www.w3.org/2000/svg"
	>
		<path
			d="M21.5806 7.19355C21.3548 6.32258 20.6774 5.64516 19.8065 5.41935C18.2581 5 12 5 12 5C12 5 5.74194 5 4.19355 5.41935C3.32258 5.64516 2.64516 6.32258 2.41935 7.19355C2 8.77419 2 12 2 12C2 12 2 15.2581 2.41935 16.8065C2.64516 17.6774 3.32258 18.3548 4.19355 18.5806C5.74194 19 12 19 12 19C12 19 18.2581 19 19.8065 18.5806C20.6774 18.3548 21.3548 17.6774 21.5806 16.8065C22 15.2581 22 12 22 12C22 12 22 8.77419 21.5806 7.19355ZM10 15V9L15.1935 12L10 15Z"
			{fill}
		/>
	</svg>
{/snippet}

<div
	class="flex justify-between pl-30 pr-20 items-end w-[600px] h-[155px] bg-[url('/images/passerby-banner.png')] bg-contain bg-no-repeat"
>
	<div class="flex grow justify-between font-bold text-[12px]">
		<a class="text-primary-300 hover:text-primary-400" href="/music">MUSIC</a>
		<a class="text-primary-300 hover:text-primary-400" href="/video">VIDEO</a>
		<a class="text-primary-300 hover:text-primary-400" href="/live">LIVE</a>
		<a class="text-primary-300 hover:text-primary-400" href="/contact">CONTACT</a>
	</div>
	<div id="social-icons" class="flex grow justify-end gap-2">
		<a href="https://www.facebook.com/passerbypop" target="_blank" rel="noopener noreferrer">
			{@render facebook(18, 'var(--color-primary-300)')}
		</a>
		<a href="https://www.youtube.com/@passerbypop" target="_blank" rel="noopener noreferrer">
			{@render youtube(18, 'var(--color-primary-300)')}
		</a>
	</div>
</div>
