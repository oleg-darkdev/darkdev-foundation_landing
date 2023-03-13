<script>
	export let progects;
</script>

<div class="progects-wrap w-full bg-info">
	<div class="progects bg-info">
		{#each progects as progect}
			<div class="progect">
				<a href={progect.link}>
					<img src={progect.logo} height="100" width="auto" alt="" />
				</a>
			</div>
		{/each}
	</div>
</div>

<style>
	@-webkit-keyframes scroll {
		0% {
			transform: translateX(0);
		}
		100% {
			transform: translateX(calc(-250px * 7));
		}
	}

	@keyframes scroll {
		0% {
			transform: translateX(0);
		}
		100% {
			transform: translateX(calc(-250px * 3));
		}
	}
	.progects-wrap {
		/* background: white; */
		box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.125);
		height: 200px;
		margin: auto;
		overflow: hidden;
		position: relative;
		/* width: 100%; */
	}
	.progects-wrap::before,
	.progects-wrap::after {
		/* background: linear-gradient(to right, white 0%, rgba(255, 255, 255, 0) 100%); */
		content: '';
		height: 200px;
		position: absolute;
		width: 200px;
		z-index: 2;
	}
	.progects-wrap::after {
		right: 0;
		top: 0;
		transform: rotateZ(180deg);
	}
	.progects-wrap::before {
		left: 0;
		top: 0;
	}
	.progects-wrap .progects {
		-webkit-animation: scroll 20s linear infinite;
		animation: scroll 20s linear infinite;
		display: flex;
		width: calc(250px * 3);
	}
	.progect {
		display: flex;
		justify-items: center;
		padding-top: 50px;
	}

	a {
		height: 100px;
		width: 400px;
	}
</style>
