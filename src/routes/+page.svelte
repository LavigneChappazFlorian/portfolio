<script lang="ts">
	import IconLink from '../components/links/iconLink.svelte';
	import PageLink from '../components/links/pageLink.svelte';
	import SocialLink from '../components/links/socialLink.svelte';
	import Project from '../components/projects/project.svelte';
	import Skill from '../components/skills/skill.svelte';
	import Work from '../components/works/work.svelte';

	export let works = [
		{
			years: '2024',
			time: 'Stage - 2 mois',
			compagny: 'ACFM Impression',
			role: 'Graphiste | Suite Adobe'
		},
		{
			years: '2020',
			time: 'Stage - 1 semaine',
			compagny: 'Xeler Informatique',
			role: 'Informaticien | Réseau | OS'
		}
	];

	export let projects = [
		{
			title: 'PopCornFlix',
			description:
				"Lors de ce projet collaboratif, mon rôle était de réaliser la partie Front-End de l'application web en utilisant le principe des composants ainsi que de gérer l'affiche des données venant de l'API REST \"TheMovieDB\".",
			goal: "Le but de ce projet était de réaliser une application web de films en React en utilisant l'API REST \"TheMovieDB\".",
			skills: ['HTML', 'CSS', 'JS', 'REACT', 'VITEJS', "Git"],
			links: [
				{
					link: 'https://github.com/LavigneChappazFlorian/popcornflix',
					icon: 'mingcute:github-fill'
				},
				{
					link: 'https://popcornflix-project.netlify.app',
					icon: 'bi:arrow-right'
				}
			],
			picture: [
				{
					src: '/img/popcornflix/logo-popcornflix.webp',
					alt: 'Logo PopCornFlix'
				}
			]
		},
		{
			title: 'Samu Social de Paris',
			description:
				"Lors de ce projet collaboratif pour le Samu Social de Paris, mon rôle était de programmer une partie de l'interface de l'application Web Mobile tout en respectant les maquettes et la charte graphique données.",
			goal: 'Le but de ce projet était de travailler la coordination entre développeurs et designers avec des outils collaboratifs comme Figma ou Git.',
			skills: ['HTML', 'CSS', 'Figma', 'Git'],
			links: [
				{
					link: 'https://github.com/Descorsiers/Brief_creatif_SAMUSOCIALPARIS/tree/Florian',
					icon: 'mingcute:github-fill'
				}
			],
			picture: [
				{
					src: '/img/samu-social-paris/illustration.png',
					alt: 'Page Info - Samu Social de Paris'
				}
			]
		},
		{
			title: "What's News",
			description:
				"Ce projet individuel consiste à réaliser un programme d'affichage en continu d’informations à destination des étudiants de l'école La Manu.",
			goal: 'Le but de ce projet est de renforcer ses compétences en PHP, notamment avec le framework Symfony, qui est beaucoup utilisé de nos jours.',
			skills: ['HTML', 'CSS', 'PHP', 'Symfony', 'Composer', 'Docker', 'Git'],
			links: [
				{
					link: 'https://github.com/LavigneChappazFlorian/whats-news',
					icon: 'mingcute:github-fill'
				}
			],
			picture: [
				{
					src: '/img/planning-symfony/whats-news.webp',
					alt: "Photo Illustration What's News"
				}
			]
		},
		{
			title: 'Magazine Nomade',
			description:
				'Ce projet individuel consiste à réaliser un magazine sur divers peuples nomades vivant aux 4 coins du monde.',
			goal: "Le but de ce projet est de mettre à profit ses compétences en graphisme, notamment avec l'utilisation de la suite Adobe, particulièrement Adobe Indesign.",
			skills: ['Adobe Illustrator', 'Adobe Indesign', 'Adobe Photoshop'],
			links: [
				{
					link: 'https://www.behance.net/gallery/194923279/Magasine-Nomade',
					icon: 'basil:behance-solid'
				}
			],
			picture: [
				{
					src: '/img/magazine-nomade/magazine.png',
					alt: 'Photo de Florian'
				}
			]
		}
	];

	export let links = [
		{
			icon: 'mingcute:github-fill',
			link: 'https://github.com/LavigneChappazFlorian',
			name: 'Github'
		},
		{
			icon: 'jam:linkedin',
			link: 'https://www.linkedin.com/in/florian-lavigne-chappaz/',
			name: 'Linkedin'
		},
		{
			icon: 'mdi:user',
			link: '/cv/lavigne-chappaz-florian-cv-stage-alternance.pdf',
			name: 'CV'
		},
		{
			icon: 'ic:baseline-email',
			link: 'mailto:florian.lavigne.chappaz@gmail.com',
			name: 'Email'
		},
		{
			icon: 'basil:behance-solid',
			link: 'https://www.behance.net/florianlavigne',
			name: 'Behance'
		},
		{
			icon: 'streamline:instagram-solid',
			link: 'https://www.instagram.com/florian.lvgchp/',
			name: 'Instagram'
		}
	];
</script>

<main>
	<section class="home">
		<div class="home__presentation">
			<div class="home__presentation__top">
				<h1>Développeur</h1>
				<PageLink link={'#projects'} name={'Projets'} />
			</div>
			<div class="home__presentation__bottom">
				<p>
					Hello 👋, je m'appelle <span>Florian Lavigne Chappaz</span> et je suis actuellement en deuxième année de
					<span>Bachelor 'Développement Web & IA'</span>. J'aime explorer de
					<span>nouvelles choses</span>
					et je suis passionné par <span>les innovations technologiques</span> et
					<span>l'intelligence artificielle</span>.
				</p>
				<h1>Full-stack</h1>
			</div>
		</div>
		<div class="home__link">
			{#each links as link}
				<SocialLink {...link} />
			{/each}
		</div>
	</section>
	<section class="about" id="about">
		<h2>... /About me ...</h2>
		<div class="about__skills">
			<div class="about__skills__left">
				<div class="about__skills__left__web">
					<Skill
						title={'Langages de programmation & No Code'}
						skills={'HTML / CMS / JS / React / ViteJS / Vue / Svelte / PHP / Symfony / MySQL / C / Python'}
					/>
				</div>
				<div class="about__skills__left__style">
					<Skill title={'Styles'} skills={'CSS / SCSS / SASS / Bootstrap / Tailwind CSS'} />
					<IconLink
						link={'https://github.com/LavigneChappazFlorian'}
						icon={'mingcute:github-fill'}
					/>
				</div>
				<div class="about__skills__left__graphism">
					<Skill
						title={'Graphisme'}
						skills={'Adobe Illustrator / Adobe Indesign / Adobe Photoshop / Adobe Premiere Pro'}
					/>
				</div>
				<div class="about__skills__left__tools">
					<p>
						Voici quelques uns des <span>principaux outils</span> que j'utilise au
						<span>quotidien</span>
					</p>
					<Skill title={'Outils'} skills={'Docker / Figma / Git / NodeJS / NPM / NPX / VSCode'} />
				</div>
			</div>
			<div class="about__skills__right">
				<img src="/img/florian.png" alt="Florian Lavigne Chappaz" />
			</div>
		</div>
		<div class="about__works">
			<h3>Work</h3>
			<div class="about__works__content">
				{#each works as work}
					<Work {...work} />
				{/each}
			</div>
		</div>
	</section>
	<section class="projects" id="projects">
		<h2>... /Projects ...</h2>
		{#each projects as project}
			<Project {...project} />
		{/each}
		<h3>Envie de voir d'autres projets ?</h3>
		<div class="projects__links">
			<SocialLink
				icon={'basil:behance-solid'}
				link={'https://www.behance.net/florianlavigne'}
				name={'Behance'}
			/>
			<SocialLink
				icon={'mingcute:github-fill'}
				link={'https://github.com/LavigneChappazFlorian'}
				name={'Github'}
			/>
		</div>
	</section>
	<section class="contact" id="contact">
		<h2>... /Contact ...</h2>
		<div class="contact__content">
			<div class="contact__content__left">
				<p>Développeur <br /> Full-stack</p>
				<h3>Florian</h3>
			</div>
			<div class="contact__content__right">
				<Skill
					title={'Site'}
					skills={'Créer par Florian / Framework utilisé : Svelte / Fait avec ❤️'}
				/>
			</div>
		</div>
		<div class="contact__link">
			{#each links as link}
				<SocialLink {...link} />
			{/each}
		</div>
	</section>
</main>

<style lang="scss">
	main {
		& .home {
			margin: 5rem;
			display: flex;
			flex-direction: column;
			gap: 2rem;

			&__presentation {
				display: flex;
				flex-direction: column;
				gap: 0.5rem;

				&__top,
				&__bottom {
					display: flex;
					flex-direction: row;
					align-items: center;
					justify-content: space-between;
				}

				&__top h1,
				&__bottom h1 {
					@include text-style('Fira Code', 7rem, bold, $light);
				}

				&__bottom {
					p {
						@include text-style('Open Sans', 1.1rem, 400, $dark-grey);
						text-align: start;
						max-width: 40%;

						span {
							color: $light-grey;
							font-style: italic;
						}
					}
				}
			}

			&__link {
				display: flex;
				flex-wrap: wrap;
				align-items: center;
				justify-content: center;
				gap: 2rem;
			}
		}

		& .about {
			margin: 5rem;
			display: flex;
			flex-direction: column;
			gap: 2rem;

			h2 {
				@include text-style('Fira Code', 0.9rem, 400, $light);
			}

			&__skills {
				display: flex;
				flex-direction: row;
				gap: 2rem;

				&__left {
					display: flex;
					flex-direction: column;
					align-items: start;
					gap: 1.5rem;
					flex: 100%;

					&__web {
						max-width: 70%;
					}

					&__style,
					&__tools {
						max-width: 70%;
						display: flex;
						flex-direction: row;
						gap: 2rem;
						align-items: center;
					}

					&__graphism {
						max-width: 70%;
					}

					&__tools {
						p {
							@include text-style('Open Sans', 1rem, 400, $dark-grey);
							text-align: start;

							span {
								color: $light-grey;
								font-style: italic;
							}
						}
					}
				}

				&__right {
					display: flex;
					align-items: center;
					justify-content: end;
					width: 100%;

					img {
						border-radius: 2rem;
						height: 600px;
						width: 450px;
						object-fit: cover;
					}
				}
			}

			&__works {
				margin: 0;

				h3 {
					@include text-style('Fira Code', 5rem, bold, $light);
					text-align: end;
				}
			}
		}

		& .projects {
			margin: 0 5rem;
			display: flex;
			flex-direction: column;
			gap: 2rem;

			h2 {
				color: $light;
				font-family: 'Fira Code';
				font-size: 0.9rem;
				font-weight: 400;
			}

			h3 {
				color: $light;
				font-family: 'Fira Code';
				font-size: 1.2rem;
				font-weight: 600;
				text-align: center;
			}

			&__links {
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: center;
				gap: 1rem;
			}
		}

		& .contact {
			margin: 5rem;

			h2 {
				@include text-style('Fira Code', 0.9rem, 400, $light);
				text-align: end;
			}

			&__content {
				margin: 2rem 0;
				display: flex;
				flex-direction: row;
				gap: 5rem;

				&__left {
					display: flex;
					flex-direction: row;
					align-items: center;
					justify-items: start;
					gap: 2.5rem;
					flex: 100%;

					p {
						@include text-style('Open Sans', 1.25rem, 400, $dark-grey);
					}

					h3 {
						@include text-style('Fira Code', 7rem, bold, $light);
					}
				}

				&__right {
					display: flex;
					align-items: center;
					justify-content: end;
					max-width: 50%;
					width: 100%;
				}
			}

			&__link {
				display: flex;
				flex-wrap: wrap;
				align-items: center;
				justify-content: center;
				gap: 2rem;
			}
		}
	}

	@media screen and (min-width: 1300px) and (max-width: 1599px) {
		main {
			& .about {
				&__skills {
					&__left {
						&__web,
						&__style,
						&__graphism,
						&__tools {
							max-width: 100%;
						}
					}
				}
			}
		}
	}

	@media screen and (max-width: 1299px) {
		main {
			.home {
				&__presentation {
					flex-direction: row;
					justify-content: center;
					gap: 2rem;

					h1 {
						font-size: 5rem;
					}

					&__top {
						flex-direction: column;
						align-items: center;
						justify-content: center;
						gap: 0.5rem;
					}

					&__bottom {
						p {
							max-width: 100%;
						}

						h1 {
							display: none;
						}
					}
				}

				&__link {
					gap: 1rem;
				}
			}

			& .about {
				&__skills {
					flex-direction: column;

					&__right {
						display: none;
					}
				}
			}

			& .contact {
				&__content {
					&__left {
						h3 {
							font-size: 5rem;
						}
					}
				}

				&__link {
					gap: 1rem;
				}
			}
		}
	}

	@media screen and (max-width: 1049px) {
		main {
			& .home {
				&__presentation {
					flex-direction: column;

					h1 {
						font-size: 3rem;
					}

					&__top {
						flex-direction: row;
						gap: 1rem;
					}
				}
			}

			& .contact {
				&__content {
					flex-direction: column;
					gap: 1rem;

					&__left {
						justify-content: center;
					}

					&__right {
						display: none;
					}
				}
			}
		}
	}

	@media screen and (max-width: 849px) {
		main {
			& .home {
				margin: 3rem;

				&__presentation {
					flex-direction: column;

					&__top {
						flex-direction: column;
					}

					&__bottom {
						display: flex;
					}
				}
			}

			& .about {
				margin: 5rem 2rem;

				&__skills {
					&__left {
						&__web,
						&__style,
						&__graphism,
						&__tools {
							max-width: 100%;
						}
					}
				}
			}

			& .projects,
			& .contact {
				margin: 5rem 2rem;
			}
		}
	}

	@media screen and (max-width: 599px) {
		main {
			& .home {
				&__presentation {
					&__top {
						font-size: 3rem;
					}
				}
			}

			& .contact {
				&__content {
					&__left {
						flex-direction: column;
						gap: 1rem;

						h3 {
							font-size: 3rem;
						}
					}
				}
			}
		}
	}
</style>
