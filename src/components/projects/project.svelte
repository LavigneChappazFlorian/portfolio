<script lang="ts">
	import IconLink from '../links/iconLink.svelte';
	import SkillBadge from '../skills/skillBadge.svelte';
	export let links: { link: string; icon: string }[] = [];
	export let skills: string[] = [];

	export let title: string;
	export let description: string;
	export let goal: string;
	export let picture: { src: string; alt: string }[] = [];
</script>

<div class="project">
	<div class="project__left">
		<h3>{title}</h3>
		<div class="project__left__badges">
			{#each skills as skill}
				<SkillBadge name={skill} />
			{/each}
		</div>
		<div class="project__left__text">
			<p>{description}</p>
			<p>{goal}</p>
		</div>
		<div class="project__left__link">
			{#each links as linkData}
				<IconLink link={linkData.link} icon={linkData.icon} />
			{/each}
		</div>
	</div>
	<div class="project__right">
		{#each picture as pictureData}
			<img src={pictureData.src} alt={pictureData.alt} />
		{/each}
	</div>
</div>

<style lang="scss">
	.project {
		margin: 2rem 0;
		display: flex;
		flex-direction: row;
		gap: 2rem;

		&__left {
			display: flex;
			flex-direction: column;
			gap: 1rem;

			h3 {
				color: $light;
				font-family: 'Open Sans';
				font-size: 1.5rem;
				font-weight: 400;
			}

			&__badges {
				display: flex;
				flex-wrap: wrap;
				gap: 1rem;
			}

			&__text {
				display: flex;
				flex-direction: column;
				gap: 1.5rem;
				margin-top: 1rem;

				p {
					color: $dark-grey;
					font-family: 'Open Sans';
					max-width: 80%;
				}
			}

			&__link {
				display: flex;
				align-items: center;
				justify-content: start;
				height: 100%;
			}
		}

		&__right {
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: end;
			gap: 0.5rem;
			width: 100%;

			img {
				border-radius: 2rem;
				width: 350px;
				max-height: 350px;
				object-fit: cover;
			}
		}
	}

	@media screen and (max-width: 849px) {
		.project {
			margin: 0;

			&__right {
				display: none;
			}
		}
	}
</style>
