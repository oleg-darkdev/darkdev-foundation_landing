<script>
	import {
		ProjectCard,
		CoordinatorCard,
		StatCard,
		WorkshopImgDarkCard,
		WorkshopImgLightCard
	} from '../components/entities';
	import { Faq, Footer, Header, GoalsList, Carousel, Gallery } from '../components/widgets';
	import { faqList, projects, stats, noOrgsWorkshops, orgWorkshopsList } from '../data';
</script>

<Header />
<section class="banner-bg md:hero lg:hero xl:hero" />

<section class="cards-wrapper flex flex min-h-screen flex-col items-center bg-gray-900">
	<div id="projects" class="flex w-full flex-col items-center pb-12 pl-1 pr-1 pt-12">
		<h2 class="mb-2 text-center text-5xl font-bold tracking-tight text-info">
			Our social projects
		</h2>
		{#each projects as project}
			<ProjectCard {project} />
		{/each}
	</div>
	<Carousel {projects} />
</section>

<section class="w-12/12 z-20 mx-auto min-h-screen bg-white px-6 pb-12 pt-12">
	<GoalsList />

	<div class="flex flex-row flex-wrap justify-center">
		<a name="contact" />
		{#each stats as stat}
			<StatCard {stat} />
		{/each}
	</div>
</section>

<!-- <section class="min-h-screen bg-info flex justify-center">
	<img src="/images/coordinator.svg" class="max-w-3xl border border-white rounded-lg" alt="" srcset="" />
</section> -->

<!-- <section class="flex flex-col items-center bg-gray-800 pt-12 pb-12">
	<CoordinatorCard />
</section> -->

<section class="bg-gray-800 px-6 py-12">
  
	<div id='offer' class="flex w-full flex-col lg:flex-row">
		<!-- bg-base-300 -->
		<div class="card rounded-box grid h-auto w-6/12 flex-grow place-items-center bg-neutral-100">
			<div class="">
				<div id="workshops-" class="mb-6 text-center">
					<h2 class="text-base font-semibold uppercase tracking-wide text-gray-700">
						Tematy warsztatów szkoleniowych
					</h2>
					<p
						class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-gray-900 sm:text-4xl"
					>
						Dla organizacji
					</p>
				</div>

				<div class="flex w-full flex-row flex-wrap justify-center">
					{#each orgWorkshopsList as workshop}
						<WorkshopImgLightCard {workshop} />
					{/each}
				</div>
			</div>
		</div>
		<div class="divider lg:divider-horizontal" />
		<div class="card rounded-box grid h-auto w-6/12 flex-grow place-items-center bg-info">
			<div id="workshops-" class="mb-6 text-center">
				<h2 class="text-base font-semibold uppercase tracking-wide text-gray-700">
					Tematy warsztatów szkoleniowych
				</h2>
				<p class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-gray-900 sm:text-4xl">
					Dla młodzieży
				</p>
			</div>

			<div class="flex w-full flex-row flex-wrap justify-center">
				{#each noOrgsWorkshops as workshop}
					<WorkshopImgDarkCard {workshop} />
				{/each}
			</div>
		</div>
	</div>
</section>

<section class="bg-gray-900 py-12">
	<!-- <h2 class="text-base font-semibold uppercase tracking-wide text-gray-700">
						lorem imosum
					</h2> -->
	<p
		class="mb-4 text-center text-3xl font-extrabold leading-8 tracking-tight text-info sm:text-4xl"
	>
		Zdjęcia z naszych wydarzeń
	</p>

	<Gallery />
</section>

<section id="faq" class="flex min-h-screen flex-col items-center justify-center bg-gray-900 pb-12">
	<Faq {faqList} />
</section>

<Footer />

<style>
	@media (max-width: 560px) {
		img {
			display: none;
		}
		.banner-bg {
			background-image: url(/images/banner_sm.svg);
			background-repeat: no-repeat;
			background-size: cover;
			height: 370px;
			background-position: center;
		}
	}
	@media (min-width: 560px) {
		.banner-bg {
			background-image: url(/images/banner.svg);
			height: 100vh;
		}
	}
</style>
