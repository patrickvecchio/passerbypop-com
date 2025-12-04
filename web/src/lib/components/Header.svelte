<script lang="ts">
    const goHome = () => {
        window.location.href = '/';
    };
</script>

{#snippet facebook(size: number, fill: string)}
	<svg width="{size}" height="{size}" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
		<path
			d="M22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.0228 5.65685 21.1599 10.4375 21.9102V14.9219H7.89844V12H10.4375V9.79688C10.4375 7.28906 11.9307 5.90625 14.2158 5.90625C15.3087 5.90625 16.4531 6.10195 16.4531 6.10195V8.59375H15.1921C13.9492 8.59375 13.5625 9.33582 13.5625 10.0977V12H16.3359L15.8926 14.8906H13.5625V21.9102C18.3431 21.1599 22 17.0228 22 12Z"
			fill="{fill}"
		/>
	</svg>
{/snippet}

{#snippet twitter(size: number, fill: string)}
	<svg width="{size}" height="{size}" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
		<path
			d="M17.7512 2.96094H20.818L14.1179 10.6187L22 21.0391H15.8284L10.9946 14.7191L5.4636 21.0391H2.39492L9.56132 12.8483L2 2.96094H8.32824L12.6976 8.73762L17.7512 2.96094ZM16.6748 19.2035H18.3742L7.40492 4.70014H5.58132L16.6748 19.2035Z"
			fill="{fill}"
		/>
	</svg>
{/snippet}
{#snippet google(size: number, fill: string)}
	<svg width="{size}" height="{size}" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
		<path
			d="M21.5939 11.0792H12.3209V13.8256H18.9768C18.6214 17.6382 15.5196 19.286 12.5148 19.286C8.70223 19.286 5.30969 16.3135 5.30969 12.0162C5.30969 7.88057 8.54068 4.74651 12.5148 4.74651C15.5519 4.74651 17.3936 6.71741 17.3936 6.71741L19.2676 4.74651C19.2676 4.74651 16.7474 2.00016 12.3856 2.00016C6.6344 1.96785 2.24023 6.78203 2.24023 11.9839C2.24023 17.0243 6.37592 22 12.4825 22C17.8783 22 21.7554 18.349 21.7554 12.8886C21.7877 11.7578 21.5939 11.0792 21.5939 11.0792Z"
			fill="{fill}"
		/>
	</svg>
{/snippet}
{#snippet youtube(size: number, fill: string)}
	<svg width="{size}" height="{size}" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
		<path
			d="M21.5806 7.19355C21.3548 6.32258 20.6774 5.64516 19.8065 5.41935C18.2581 5 12 5 12 5C12 5 5.74194 5 4.19355 5.41935C3.32258 5.64516 2.64516 6.32258 2.41935 7.19355C2 8.77419 2 12 2 12C2 12 2 15.2581 2.41935 16.8065C2.64516 17.6774 3.32258 18.3548 4.19355 18.5806C5.74194 19 12 19 12 19C12 19 18.2581 19 19.8065 18.5806C20.6774 18.3548 21.3548 17.6774 21.5806 16.8065C22 15.2581 22 12 22 12C22 12 22 8.77419 21.5806 7.19355ZM10 15V9L15.1935 12L10 15Z"
			fill="{fill}"
		/>
	</svg>
{/snippet}

<div
	class="flex justify-between pl-18 pr-20 items-end w-[600px] h-[155px] bg-[url('/images/passerby-banner.png')] bg-contain bg-no-repeat"

>
	<div class="flex grow justify-between font-bold text-[12px]">
		<a class=" text-gray-500 hover:text-primary-500" href="/music">MUSIC</a>
		<a class=" text-gray-500 hover:text-primary-500" href="/video">VIDEO</a>

		<div class=" text-gray-500 hover:text-primary-500">LIVE</div>
		<div class=" text-gray-500 hover:text-primary-500">MERCH</div>
		<div class=" text-gray-500 hover:text-primary-500">CONTACT</div>
	</div>
	<div id="social-icons" class="flex grow justify-end gap-2">
        <a href="https://www.facebook.com/passerbypop" target="_blank" rel="noopener noreferrer">
            {@render facebook(18, 'var(--color-gray-700)')}
        </a>
        <a href="https://twitter.com/passerbypop" target="_blank" rel="noopener noreferrer">
            {@render twitter(18, 'var(--color-gray-700)')}
        </a>
        <a href="https://plus.google.com/u/1/115637981182265104973" target="_blank" rel="noopener noreferrer">
            {@render google(18, 'var(--color-gray-700)')}
        </a>
        <a href="https://www.youtube.com/@passerbypop" target="_blank" rel="noopener noreferrer">
            {@render youtube(18, 'var(--color-gray-700)')}
        </a>
	</div>
</div>
