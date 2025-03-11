<script lang="ts">
	import Icon from '@iconify/svelte';
	export let icon: string = 'default';
	export let link: string = 'default';
	export let name: string = 'default';
</script>

<div class="link">
	<div class="link__item">
		<a href={link} aria-label="link" target="_blank">
			<span>
				<Icon {icon} />
			</span>
			{name}
		</a>
	</div>
</div>

<style lang="scss">
	.link {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		font-family: 'Open Sans';

		a {
			display: flex;
			flex-direction: row;
			gap: 10px;
			border: 1px solid $light-grey;
			border-radius: 2rem;
			padding: 0.75rem 2rem;
			color: $light-grey;
			font-size: 1.2rem;
			font-style: italic;
			text-decoration: none;

			span {
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: center;
				color: $light;
				font-size: 1.5rem;
			}
		}
	}

	.link:hover {
		background: $light;
		border-radius: 2rem;

		a,
		span {
			color: $dark-grey;
		}
	}
</style>
