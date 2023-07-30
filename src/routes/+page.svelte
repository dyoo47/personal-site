<script lang="ts">
	import Fa from 'svelte-fa';
	import { faGithub, faLinkedin, faTwitter } from '@fortawesome/free-brands-svg-icons';
	import { faCode, faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import Button from '../components/Button.svelte';
	import Link from '../components/Link.svelte';
	import ExperienceCard from '../components/ExperienceCard.svelte';
	import EducationCard from '../components/EducationCard.svelte';
</script>

<svelte:head><title>Daniel Yoo</title></svelte:head>
<div class="container px-10 lg:px-20 mx-auto grid align-top grid-cols-1 lg:grid-cols-2">
	<div class="lg:h-screen py-20 grid lg:sticky lg:top-0">
		<div>
			<h1 class="h1 text-6xl">Daniel Yoo</h1>
			<div class="my-2">
				<span class="h4">SWE Intern at Liferay</span>
			</div>
			<p class="text-slate-400">
				Frontend developer, computer graphics enthusiast,
				<br /> avid boulderer/guitar player.
			</p>
			<div class="my-20">
				<Link href="#about">ABOUT</Link>
				<Link href="#experience">EXPERIENCE</Link>
				<Link href="#projects">PROJECTS</Link>
			</div>
		</div>
		<div class="self-end flex mt-5">
			<Button href="https://github.com/dyoo47/personal-site"><Fa icon={faCode} /></Button>
			<Button href="https://github.com/dyoo47"><Fa icon={faGithub} /></Button>
			<Button href="https://www.linkedin.com/in/danielnyoo/"><Fa icon={faLinkedin} /></Button>
			<Button href="https://twitter.com/danny_yoo19"><Fa icon={faTwitter} /></Button>
		</div>
	</div>
	<div class="text-slate-400 pb-20">
		<section id="about" class="pt-20">
			<div class="px-4">
				<span>
					I wrote my first ever line of code in grade school for a Minecraft mod. Since then, my
					curiosity has led me to explore diverse domains— web development, <a
						href="https://ldjam.com/users/klekky/games"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300"
						>gamedev,
					</a>computer graphics, and robotics— just to name a few. I take great pleasure in
					immersing myself in novel concepts, readily embracing challenges and actively engaging in
					practical implementation.
					<br />
					<br />
					When I'm not coding I like to destress(?) by five stacking with friends in
					<a
						href="https://tracker.gg/valorant/profile/riot/STARCHU%23NA99/overview"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">Valorant</a
					>
					or climbing at a
					<a
						href="https://climbhangar18.com/orange/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">local gym.</a
					>
					Occasionally I play guitar in a futile attempt to learn Polyphia songs.
				</span>
			</div>
		</section>
		<div class="pt-28">
			<section id="experience" class="pb-28">
				<EducationCard
					description="Math-CS Major, 3.4 GPA"
					span="2020 - 2023"
					title="UC San Diego"
				/>
				<ExperienceCard
					href="https://www.liferay.com/"
					span="2023 - present"
					location="Diamond Bar, CA"
					title="SWE Intern - Liferay, Inc."
					description="Full-time intern position in the Global Services consulting team, tasked
						with creating an out-facing portal for a government financial department.
						Designed and implemented 3 MVC web portlets under the OSGi specification
						as extensions of Liferay’s main open-source product (Liferay DXP),
						populated front-end React components with a mySQL database."
					skills={['Java', 'JavaScript', 'React', 'OSGi', 'Liferay DXP', 'Jira', 'Github Actions']}
				/>
				<ExperienceCard
					href="https://www.thebluealliance.com/team/7157/2020"
					span="SEP 2017 - 2020"
					location="Brea, CA"
					title="Lead Programmer - FRC 7157 μBotics"
					description="Developed two competition bots with multi-threaded autonomous subroutines,
						closed-loop control (PID), and an award-winning vision pipeline.
						Integrated a suite of motor controllers and a Linux coprocessor (NVIDIA
						Jetson Nano) over a network-table based interface. Taught and led a team of 8 peers 
						throughout an intense twelve week sprint of competition, collaborated using git source control."
					links={[
						{
							label: 'Creativity Award',
							href: 'https://www.firstinspires.org/resource-library/frc/awards-based-on-machine-creativity-innovation'
						}
					]}
					skills={['Java', 'Python', 'git', 'Closed loop control', 'OpenCV', 'Ubuntu']}
				/>
				<a
					href="/"
					on:click={() => {
						window.open('img/resume.pdf', '_blank', 'fullscreen=yes');
					}}
					class="flex w-fit group"
					><h6
						class="h6 text-primary-50 pt-4 pl-4 group-hover:underline transition duration-150 ease-in-out"
					>
						View Full Resume <Fa
							class="inline ml-2 group-hover:translate-x-1 transition duration-150 ease-in-out"
							icon={faArrowRight}
							scale={0.8}
						/>
					</h6></a
				>
			</section>
			<section id="projects" class="pb-20">
				<ExperienceCard
					href="https://github.com/dyoo47/svo-raytracer"
					image="img/colorblobs.png"
					title="svo-raytracer"
					description="Realtime Java/LWJGL voxel path tracer based on the paper Efficient Sparse
					Voxel Octrees by Samuli Laine and Tero Karras. 2 bounces 1080p ~30fps, up to 2048^3 
					world size, implemented on GPU. Created a custom octree layout to maximize memory 
					coherency/efficiency and minimize ray traversal time."
					links={[
						{
							label: 'Efficient Sparse Voxel Octrees',
							href: 'https://users.aalto.fi/~laines9/publications/laine2010i3d_paper.pdf'
						}
					]}
					skills={[
						'Java',
						'LWJGL',
						'OpenGL',
						'GLSL',
						'GPU',
						'Octrees',
						'Multi-threading',
						'Path tracer'
					]}
				/>
				<ExperienceCard
					href="#"
					image="img/fearsha.png"
					title="Fearsha Frontend"
					disableLink
					description="Developed React/TS frontend for a payment and booking service designed for day-of 
						booking and stat tracking in the escape games niche. 
						Implemented static page rendering with Next.js, created queries in GraphQL to populate 
						front-end components from a PostgreSQL database. Supervised and contributed to a 35k lines codebase."
					skills={[
						'JavaScript',
						'TypeScript',
						'React',
						'Next.js',
						'GraphQL',
						'Hasura',
						'HTML',
						'SCSS'
					]}
				/>
				<ExperienceCard
					href="https://www.thebluealliance.com/team/7157/2020"
					image="img/frc2020.png"
					title="FRC 2019/2020 - Robot Code"
					description="Led the software development of two competition bots. Highlights include an award-winning vision pipeline,
						field position based shot calculation, and a PID controlled climb mechanism."
					links={[
						{ label: 'Github Repo', href: 'https://github.com/Mubotics7157' },
						{ label: '2019 Recap', href: 'https://www.youtube.com/watch?v=QehlMgzTxbY' },
						{ label: '2020 Recap', href: 'https://www.youtube.com/watch?v=Y51J-qdgaS8' }
					]}
					skills={['Java', 'Python', 'git', 'Closed loop control', 'OpenCV', 'Ubuntu']}
				/>
			</section>
			<section>
				<p class="text-sm">
					Built in <a
						href="https://svelte.dev/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">Svelte</a
					>
					using
					<a
						href="https://tailwindcss.com/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300"
					>
						Tailwind CSS</a
					>
					and
					<a
						href="https://www.skeleton.dev/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300"
					>
						Skeleton UI.</a
					>
					Layout heavily inspired by
					<a
						href="https://brittanychiang.com/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">Brittany Chiang.</a
					>
					Deployed using
					<a
						href="https://kit.svelte.dev/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">SvelteKit.</a
					>
					Icons from
					<a
						href="https://fontawesome.com/"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">Font Awesome.</a
					>
				</p>
			</section>
		</div>
	</div>
</div>
