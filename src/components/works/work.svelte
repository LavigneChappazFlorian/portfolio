<script lang="ts">
	export let years: string;
	export let time: string;
	export let compagny: string;
	export let role: string;
</script>

<div class="work">
	<div class="work__left">
		<span>{years}</span>
		<small>{time}</small>
	</div>
	<div class="work__right">
		<span>{compagny}</span>
		<span>{role}</span>
	</div>
</div>

<style lang="scss">
	.work {
		display: flex;
		align-items: center;
		gap: 2rem;
		border-top: 1px solid $light-grey;
		padding: 1rem 0;

		&:last-child {
			border-bottom: 1px solid $light-grey;
		}

		&__left {
			display: flex;
			flex-direction: column;
			color: $light-grey;
			font-family: 'Open Sans';
			width: 30%;
			min-width: 80px;

			span {
				font-size: 1.5rem;
			}

			small {
				color: $dark-grey;
			}
		}

		&__right {
			flex: 1;
			display: flex;
			justify-content: space-between;

			span:nth-child(1) {
				color: $light-grey;
				font-family: 'Open Sans';
				font-size: 1.25rem;
			}

			span:nth-child(2) {
				font-size: 1.25rem;
				color: $light-grey;
				font-family: 'Fira Code';
			}
		}
	}

	@media screen and (max-width: 599px) {
		.work {
			&__right {
				flex-direction: column;
				gap: 1rem;
			}
		}
	}
</style>
