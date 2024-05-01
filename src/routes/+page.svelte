<script>
	import ProgectCard from '../components/ProgectCard.svelte';
	import Faq from '../components/Faq.svelte';
	import Footer from '../components/Footer.svelte';
	import Header from '../components/Header.svelte';
	import StatCard from '../components/StatCard.svelte';
	import GoalsList from '../components/GoalsList.svelte';
	import Coordinator from '../components/Coordinator.svelte';
	import Carousel from '../components/Carousel.svelte';
	import Gallery from '../components/Gallery.svelte';
	import WorkshopImgLightCard from '../components/WorkshopImgLightCard.svelte';
	import WorkshopImgDarkCard from '../components/WorkshopImgDarkCard.svelte';

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
		},
		{
			title: 'AgileKIT Community',
			description: [
				'Społeczność AgileKIT zaprasza praktyków wszystkich zawodów do wspólnej edukacji, rozrywki i rozwoju - zarówno poprzez spotkania wirtualne, jak i bezpośrednie.'
			],
			logo: '/images/logos/agileKit.svg',
			link: 'https://agile-kit.vercel.app/',
			flip: 'right'
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
			title: 'Zorganizowane lokalne inicjatywy',
			count: 7,
			fade: 'up'
		},
		{
			title: 'Wsparcie dla NGO',
			count: 20,
			fade: 'down'
		}
	];

	const boardgamesWorkshopsList = [
		{
			id: 0,
			img: 'boardgame-mechanics.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'boardgame-design.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'boardgame-prototype.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'tech-site.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'tech-3d.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'tech-cnc.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		}
	];

	const itWorkshopsList = [
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		},
		{
			id: 0,
			img: 'it-del.svg',
			title: 'Lorem ipsum is placeholder',
			desc: 'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries.',
			link: '/'
		}
	];
</script>

<Header />
<section class="banner-bg md:hero lg:hero xl:hero " />

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

<!-- <section class="flex flex-col items-center bg-gray-800 pt-12 pb-12">
	<Coordinator />
</section> -->

<section class="bg-gray-800 p-10">
	<div class="flex w-full flex-col lg:flex-row">
		<!-- bg-base-300 -->
		<div class="card rounded-box grid h-auto w-6/12 flex-grow place-items-center bg-neutral-100">
			<div class="">
				<div id="workshops-" class="mb-6 text-center">
					<h2 class="text-base font-semibold uppercase tracking-wide text-gray-700">
						предлагаемые темы обучающих воркшопов
					</h2>
					<p
						class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-gray-900  sm:text-4xl"
					>
						Для организаций
					</p>
				</div>

				<div class="flex w-full flex-row flex-wrap justify-center">
					{#each itWorkshopsList as workshop}
						<WorkshopImgLightCard {workshop} />
					{/each}
				</div>
			</div>
		</div>
		<div class="divider lg:divider-horizontal" />
		<div class="card rounded-box grid h-auto w-6/12 flex-grow place-items-center bg-info">
			<div id="workshops-" class="mb-6 text-center">
				<h2 class="text-base font-semibold uppercase tracking-wide text-gray-700">
					предлагаемые темы обучающих воркшопов
				</h2>
				<p class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-gray-900  sm:text-4xl">
					Для молодёжи
				</p>
			</div>

			<div class="flex w-full flex-row flex-wrap justify-center">
				{#each boardgamesWorkshopsList as workshop}
					<WorkshopImgDarkCard {workshop} />
				{/each}
			</div>
		</div>
	</div>
</section>

<section class="bg-info pt-10" />

<Gallery />

<section
	id="faq"
	class="flex min-h-screen flex-col items-center justify-center bg-gray-900 p-4 pt-12 pb-12"
>
	<!-- <div class="flex max-w-2xl  rounded-lg border border-info"> -->
	<!-- <img src="/images/faq.svg" class="m-1 h-full max-w-sm rounded-lg" alt="" srcset="" /> -->
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
