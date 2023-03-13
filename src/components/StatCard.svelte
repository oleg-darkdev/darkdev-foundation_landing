<script>
	export let stat;
</script>

<div 	data-aos="fade-{stat.fade}"
	data-aos-offset="300"
	data-aos-duration="500"
  class="m-2 stat-card w-36 rounded-2xl bg-white p-4 shadow-lg dark:bg-gray-800">
	<div class="flex items-center">
		<span class="text-md ml-2  text-info">{stat.title}</span>
	</div>
	<div class="flex flex-col justify-start">
		<p class="my-4 text-left text-5xl font-bold text-info">{stat.count}</p>
	</div>
</div>

<style>
	.stat-card:nth-child(odd) {
		margin-bottom: 3%;
	}
	.stat-card:nth-child(even) {
		margin-top: 3%;
	}
</style>
