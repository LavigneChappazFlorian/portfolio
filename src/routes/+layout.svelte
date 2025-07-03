<script lang="ts">
	import type { Snippet } from 'svelte';
	import { Hamburger } from 'svelte-hamburgers';
	import '../lib/scss/main.scss';
	import { fly } from 'svelte/transition';

	let open = $state(true);

	type Props = {
		children: Snippet;
	};

	const { children }: Props = $props();
</script>

<svelte:head>
	<script
		type="module"
		src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"
	></script>
	<script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
	<title>Portfolio | Florian Lavigne Chappaz</title>
</svelte:head>

<div class="banner">
	<span>Important ! Un nouveau portfolio est en cours de développement, il sera disponible prochainement.</span>
</div>

<header>
	<nav class="nav">
		<div class="nav__left">
			<span>
				<a href="/" aria-label="home">Florian</a>
			</span>
		</div>
		<div class="nav__center">
			<ul>
				<li><a href="#about" aria-label="about">A propos</a></li>
				<li><a href="#projects" aria-label="projects">Projets</a></li>
				<li><a href="#contact" aria-label="contact">Contact</a></li>
			</ul>
		</div>
		<div class="nav__right">
			<span id="en">En</span>
			<span class="isActive" id="fr">Fr</span>
		</div>
		<div class="nav__menu">
			<Hamburger bind:open ariaControls="nav" type="collapse" --color="white" />
			{#if open}
				<ul id="nav" class="nav__menu__open" transition:fly={{ y: -15 }}>
					<li><a href="#about" aria-label="about">A propos</a></li>
					<li><a href="#projects" aria-label="projects">Projets</a></li>
					<li><a href="#contact" aria-label="contact">Contact</a></li>
				</ul>
			{/if}
		</div>
	</nav>
</header>

{@render children()}

<style lang="scss">
	.banner {
		background: $light;
		color: $dark;
		padding: 1rem;
		text-align: center;
	}
	header {
		position: sticky;
		top: 0;
		background: $dark;
		padding: .25rem;
		box-shadow: 0 0 10px black;

		& .nav {
			margin: 1.5rem;
			display: flex;
			align-items: center;
			justify-content: space-around;
			font-family: 'Fira Code';

			&__left {
				a {
					text-decoration: none;
					font-size: 1.5rem;
					color: $light;
				}
			}

			&__center {
				ul {
					list-style-type: none;
					display: flex;
					flex-direction: row;
					align-items: center;
					justify-content: center;
					gap: 2rem;

					li {
						a {
							text-decoration: none;
							font-size: 1rem;
							color: $light;
						}

						a:hover {
							border-bottom: 1px solid $light;
						}
					}
				}
			}

			&__right {
				display: flex;
				flex-direction: row;
				gap: 1rem;

				span {
					position: relative;
					color: $light;
					cursor: pointer;
				}

				span.isActive {
					border-bottom: 1px solid $light;
				}

				span:hover {
					border-bottom: 1px solid $light;
				}
			}

			&__menu {
				display: none;
			}
		}
	}

	@media screen and (max-width: 849px) {
		header {
			padding: 5px;

			& .nav {
				&__center,
				&__right {
					display: none;
				}

				&__menu {
					position: relative;
					z-index: 1;
					display: flex;
					align-items: center;

					ul {
						padding: 2rem;
						position: absolute;
						z-index: 1;
						top: 100%;
						left: 50%;
						transform: translateX(-50%);
						list-style: none;
						display: flex;
						flex-direction: column;
						gap: 1rem;
						background: $dark;
						box-shadow: 0 0 20px 0 black;

						li {
							a {
								white-space: nowrap;
								text-decoration: none;
								font-size: 1rem;
								color: $light;
							}
						}
					}
				}
			}
		}
	}
</style>
