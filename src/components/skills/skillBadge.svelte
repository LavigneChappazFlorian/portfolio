<script lang="ts">
	export let name: string = 'default';
</script>

<div class="link">
	<div class="link__item">
		<span>
			{name}
		</span>
	</div>
</div>

<style lang="scss">
	.link {
		border: 1px solid $light-grey;
		border-radius: 2rem;
		max-width: fit-content;
		padding: .25rem 1rem;
		font-family: 'Fira Code';

		span {
			color: $light-grey;
			font-size: .9rem;
		}
	}
</style>
