<script lang="ts">
	import Icon from '@iconify/svelte';
	export let link: string = 'default';
	export let name: string = 'default';
</script>

<div class="link">
	<div class="link__text">
		<a href={link} aria-label="link">{name}</a>
	</div>
	<div class="link__arrow">
		<a href={link} aria-label="link"><Icon icon="bi:arrow-right" /></a>
	</div>
</div>

<style lang="scss">
	.link {
		display: flex;
		flex-direction: row;
		gap: 10px;
		font-family: 'Open Sans';
		text-align: center;

		&__text {
			display: flex;
			align-items: center;

			a {
				padding: 1rem 8rem;
				border: 1px solid transparent;
				border-radius: 2rem;
				background-color: $light;
				color: $dark;
				text-decoration: none;
				font-size: 1.2rem;
				font-style: italic;
			}
		}

		&__arrow {
			display: flex;
			align-items: center;

			a {
				padding: 1rem 1.25rem;
				border: 1px solid transparent;
				border-radius: 50%;
				background-color: $light;
				color: $dark;
				text-decoration: none;
				font-size: 1.2rem;
				font-style: italic;
			}
		}
	}
</style>
