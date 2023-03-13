<script>
	import ProgectCard from '../components/ProgectCard.svelte';
	import Faq from '../components/Faq.svelte';
	import Footer from '../components/Footer.svelte';
	import Header from '../components/Header.svelte';
	import StatCard from '../components/StatCard.svelte';
	import GoalsList from '../components/GoalsList.svelte';
	import Coordinator from '../components/Coordinator.svelte';
	import Carousel from '../components/Carousel.svelte';

	import faqList from '../data/landingFaqList';

	const progects = [
		{
			title: '44FabLab',
			description: [
				'Otwarta przestrzeń dla twórczości technicznej i programowania oraz tworzenia edukacyjnych gier planszowych.'
			],
			logo: '/images/logos/44fab_lab.svg',
			link: 'https://44hackerspace.vercel.app/',
			flip: 'right'
		},
		{
			title: 'ITingo',
			description: [
				'ITingo to platforma internetowa, która łączy IT wolontariuszy, organizacje pozarządowe, biznes i startupy - w celu dostarczenia projektów IT online.'
			],
			logo: '/images/logos/itingo.svg',
			link: 'https://itingo.vercel.app/',
			flip: 'right'
		},

		{
			title: 'Yellow elephant',
			description: [
				'Comiesięczny turniej szachów klasycznych zarówno dla amatorów jak i tych bardziej zaawansowanych graczy.',
				'Turniej odbywa się każda środa w pierwszym tygodniu miesiąca.'
			],
			logo: '/images/logos/yellow_elephant.svg',
			link: 'https://yellow-elephant.vercel.app/',
			flip: 'left'
		},
		{
			title: '44games',
			description: ['Tworzenie, rozwój i produkcja prototypów edukacyjnych gier planszowych.'],
			logo: '/images/logos/44_cubes.svg',
			link: 'https://44games.vercel.app/',
			flip: 'left'
		}
	];

	const statisticsData = [
		{
			title: 'Stworzone gier planszowych',
			count: 16,
			fade: 'up'
		},
		{
			title: 'Zorganizowane warsztaty',
			count: 40,
			fade: 'down'
		},
		{
			title: 'Организовано локальных иннициатив',
			count: 7,
			fade: 'up'
		},
		{
			title: 'Поддержано НГО',
			count: 20,
			fade: 'down'
		}
	];
</script>

<Header />
<section class="banner-bg lg:hero md:hero xl:hero " />

<section class="cards-wrapper flex flex min-h-screen flex-col items-center bg-gray-900 ">
	<div id="progects" class="flex w-full flex-col items-center pb-12 pt-12 pr-1 pl-1">
		<h2 class="mb-2 text-center text-5xl font-bold tracking-tight text-info">
			Our social progects
		</h2>
		{#each progects as progect}
			<ProgectCard {progect} />
		{/each}
	</div>
	<Carousel {progects} />
</section>

<section class="w-12/12 z-20 mx-auto min-h-screen  bg-white px-6 pt-12 pb-12">
	<GoalsList />

	<div class="flex flex-row flex-wrap  justify-center">
		<a name="contact" />
		{#each statisticsData as stat}
			<StatCard {stat} />
		{/each}
	</div>
</section>

<!-- <section class="min-h-screen bg-info flex justify-center">
	<img src="/images/coordinator.svg" class="max-w-3xl border border-white rounded-lg" alt="" srcset="" />
</section> -->

<section class="flex flex-col items-center bg-gray-800 pt-12 pb-12">
	<Coordinator />
</section>

<section
	id="faq"
	class="flex min-h-screen flex-row flex-wrap justify-center  bg-gray-900 p-4 pt-12 pb-12"
>
	<!-- <div class="flex max-w-2xl  rounded-lg border border-info"> -->
	<img src="/images/faq.svg" class="m-1 h-full max-w-sm rounded-lg" alt="" srcset="" />
	<div id="faq" class="flex flex-col">
		<Faq {faqList} />
	</div>
	<!-- </div> -->
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
