<script>
	export let progect;
</script>

<a
	data-aos="flip-{progect.flip}"
	data-aos-offset="170"
	data-aos-duration="500"
	href={progect.link}
	class="m-2 flex max-w-md flex-col rounded-lg border border-gray-200 bg-info p-4 text-gray-500 shadow-md dark:border-gray-700 dark:text-gray-400 sm:p-6"
>
	<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900">
		{progect.title}
	</h5>
	{#each progect.description as desc}
		<p class="mb-3 font-normal leading-tight text-gray-700 ">
			{desc}
		</p>
	{/each}
	<button
		type="button"
		class="inline-flex w-fit items-center justify-center rounded-lg bg-gray-900 px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-info hover:text-gray-900 focus:outline-none "
		>Read more <svg
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			viewBox="0 0 24 24"
			stroke-width="1.5"
			stroke="currentColor"
			class="ml-2 h-5 w-5"
			><path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"
			/></svg
		></button
	>
</a>

<!--
<a
	href={progect.link}
	class="m-2 flex max-w-md flex-col rounded-lg border border-gray-200 bg-gray-900 text-gray-500 shadow-md md:max-w-xl md:flex-row lg:max-w-2xl"
>
	<img
		class="h-96 w-full rounded-t-lg object-cover md:h-auto md:w-48 md:rounded-none md:rounded-l-lg"
		src={progect.img}
		alt={progect.title}
	/>
	<div class="p-4 sm:p-6  ">
		<h5 class="mb-2 text-2xl font-bold tracking-tight  text-white">
			{progect.title}
		</h5>
		{#each progect.description as desc}
			<p class="mb-3 font-normal leading-tight text-gray-400 ">
				{desc}
			</p>
		{/each}
		<button
			type="button"
			class="mt-6 inline-flex w-fit items-center justify-center rounded-lg px-5 py-2.5 text-center text-sm font-medium text-white hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
			>Read more <svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="1.5"
				stroke="currentColor"
				class="ml-2 h-5 w-5"
				><path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"
				/></svg
			></button
		>
	</div></a
> -->
<style>
	@media (min-width: 560px) {
		a:nth-child(odd) {
			margin-right: 10%;
		}
		a:nth-child(even) {
			margin-left: 10%;
		}
	}
</style>
