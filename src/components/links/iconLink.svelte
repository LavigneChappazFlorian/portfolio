<script lang="ts">
	import Icon from '@iconify/svelte';
	export let link: string;
	export let icon: string;
</script>

<div class="link">
	<div class="link__icon">
		<a href={link} aria-label="link" target="_blank"><Icon {icon} /></a>
	</div>
</div>

<style lang="scss">
	.link {
		&__icon {
			display: flex;
			align-items: center;
			justify-content: center;
			border: 1px solid $light-grey;
			border-radius: 50px;
			padding: 1rem 1.25rem;

			a {
				text-decoration: none;
				color: $light;
				font-size: 1.5rem;
			}
		}
	}

	.link:hover {
		background: $light;
		border-radius: 2rem;

		a {
			color: $dark-grey;
		}
	}
</style>
