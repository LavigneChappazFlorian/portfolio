<script lang="ts">
	import type { Snippet } from 'svelte';
	import '../lib/scss/main.scss';

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
	</nav>
</header>

{@render children()}

<style lang="scss">
	header {
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
		}
	}
</style>
