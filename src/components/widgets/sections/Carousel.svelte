<script>
	export let projects;
</script>

<div class="projects-wrap w-full bg-info">
	<div class="projects bg-info">
		{#each projects as project}
			<div class="project">
				<a href={project.link}   target="_blank">
					<img src={project.logo} height="100" width="auto" alt="" />
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
	.projects-wrap {
		/* background: white; */
		box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.125);
		height: 200px;
		margin: auto;
		overflow: hidden;
		position: relative;
		/* width: 100%; */
	}
	.projects-wrap::before,
	.projects-wrap::after {
		/* background: linear-gradient(to right, white 0%, rgba(255, 255, 255, 0) 100%); */
		content: '';
		height: 200px;
		position: absolute;
		width: 200px;
		z-index: 2;
	}
	.projects-wrap::after {
		right: 0;
		top: 0;
		transform: rotateZ(180deg);
	}
	.projects-wrap::before {
		left: 0;
		top: 0;
	}
	.projects-wrap .projects {
		-webkit-animation: scroll 20s linear infinite;
		animation: scroll 20s linear infinite;
		display: flex;
		width: calc(250px * 3);
	}
	.project {
		display: flex;
		justify-items: center;
		padding-top: 50px;
	}

	a {
		height: 100px;
		width: 400px;
	}
</style>
