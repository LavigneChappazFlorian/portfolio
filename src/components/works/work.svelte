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
	<div class="work__center">
		<span>{compagny}</span>
	</div>
	<div class="work__right">
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

		&__center {
			flex: 1;
			text-align: left;

			span {
				color: $light-grey;
				font-family: 'Open Sans';
				font-size: 1.25rem;
			}
		}

		&__right {
			width: 30%;
			text-align: right;

			span {
				font-size: 1.25rem;
				color: $light-grey;
				font-family: 'Fira Code';
			}
		}
	}
</style>
