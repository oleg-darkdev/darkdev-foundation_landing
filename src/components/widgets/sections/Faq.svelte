<script>
	export let faqList;
</script>

<!-- 		data-aos="flip-down"
		data-aos-delay="100"
		data-aos-duration="1400"
		data-aos-once="false"
		data-aos-mirror="true"
 -->
{#each faqList as faq}
	<div
		class=" max-w-4xl w-full bg-info rounded-lg my-2 "
	>
		<p
			class="w-full min-h-16 h-auto max-h-40 rounded-lg "
			on:click={() => (faq.showText = !faq.showText)}
			id="accordion-collapse-heading-1"
		>
			<button
				type="button"
				class="flex  rounded-lg w-full items-center justify-between border border-b-0 border-gray-200 bg-info p-5 text-left  font-medium text-gray-900 hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 "
			>
				<span>{faq.title} <i class="icon-question color-viol" /> </span>
				<span><i class="{!faq.showText ? 'icon-arrow-down' : 'icon-arrow-up'} color-viol" /></span>
				<!-- <svg data-accordion-icon="" class="w-6 h-6 rotate-180 shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg> -->
			</button>
		</p>
		{#if faq.showText}
			<div
				id="accordion-collapse-body-1"
				class="bg-white "
				aria-labelledby="accordion-collapse-heading-1"
			>
				<div
					class="border border-b-0 border-gray-200 p-5 font-light dark:border-gray-700 dark:bg-gray-900"
				>
					{#each faq.desctiption as desctiption}
						<p class="mb-2 text-gray-300">{desctiption}</p>
					{/each}
				</div>
			</div>
		{/if}
	</div>
{/each}
