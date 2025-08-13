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
<div class="lg:container px-10 lg:px-20 mx-auto grid align-top grid-cols-1 lg:grid-cols-2">
	<div class="lg:h-screen lg:pb-20 pt-20 grid lg:sticky lg:top-0 px-4">
		<div class="md:w-1/2 lg:w-full">
			<h1 class="h1 text-6xl">Daniel Yoo</h1>
			<div class="my-2">
				<span class="h4">dyoo4747@gmail.com</span>
			</div>
			<p class="text-slate-400 lg:pr-28">
				Frontend developer, computer graphics enthusiast, avid boulderer/guitar player.
			</p>
			<div class="my-20 max-lg:hidden">
				<Link href="#about">ABOUT</Link>
				<Link href="#experience">EXPERIENCE</Link>
				<Link href="#projects">PROJECTS</Link>
			</div>
		</div>
		<div class="self-end flex mt-5 max-lg:pb-28">
			<Button ariaLabel="View this project on GitHub" href="https://github.com/dyoo47/personal-site"
				><Fa icon={faCode} /></Button
			>
			<Button ariaLabel="View my GitHub profile" href="https://github.com/dyoo47"
				><Fa icon={faGithub} /></Button
			>
			<Button ariaLabel="View my LinkedIn profile" href="https://www.linkedin.com/in/danielnyoo/"
				><Fa icon={faLinkedin} /></Button
			>
			<Button ariaLabel="View my Twitter profile" href="https://twitter.com/danny_yoo19"
				><Fa icon={faTwitter} /></Button
			>
		</div>
	</div>
	<div class="text-slate-400 pb-20">
		<section id="about" class="lg:pt-20">
			<div class="px-4 mb-8 lg:hidden">
				<span class="text-sm tracking-widest font-bold text-primary-50">ABOUT</span>
			</div>
			<div class="px-4">
				<span>
					I wrote my first ever line of code in grade school for a Minecraft mod. Since then, my
					curiosity has led me to explore many domains— web development, <a
						href="https://ldjam.com/users/klekky/games"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300"
						>gamedev,
					</a>computer graphics, and robotics— just to name a few. Confronting formidable challenges
					and steep learning curves is my bread and butter.
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
				<div class="px-4 mb-8 lg:hidden">
					<span class="text-sm tracking-widest font-bold text-primary-50"
						>EXPERIENCE & EDUCATION</span
					>
				</div>
				<EducationCard
					description="B.S. in Mathematics-Computer Science, 3.4 GPA"
					span="2020 - 2023"
					title="UC San Diego"
				/>

				<ExperienceCard
					href="https://dwe.ai/pages/about"
					span="APR 2025 - NOW"
					location="San Diego, CA"
					title="DeepWater Exploration"
					subscript="Software Engineer"
					description="Building the future of subsea computer vision!"
					skills={['C++', 'OpenGL']}
				/>
				<ExperienceCard
					href="https://theimmersivecompany.com/"
					span="OCT 2024"
					location="Los Angeles, CA"
					title="The Immersive Company"
					subscript="Software Engineer (Contract)"
					description="Built an interactive 3D intro sequence for a flagship VR immersive video app in RealityKit/visionOS. 
						Engineered a custom animation engine leveraging 3D Bézier curves for smooth and dynamic visuals."
					skills={['Swift', 'RealityKit', 'visionOS', 'Apple Vision Pro']}
				/>
				<ExperienceCard
					href="#"
					span="MAR - JUN 2024"
					location="Los Angeles, CA"
					title="Stealth Startup"
					subscript="Software Engineer (Contract)"
					description="Designed and implemented intuitive user-facing pages in Angular for a school admin tool. Architected end-to-end services
						using Azure functions and an Azure SQL database."
					skills={['Angular', 'Azure Functions', 'SQL', 'Java']}
				/>
				<ExperienceCard
					href="https://www.liferay.com/"
					span="MAY - DEC 2023"
					location="Diamond Bar, CA"
					title="Liferay, Inc."
					subscript="Associate Software Consultant"
					description="Full-stack development/consulting position. Tasked with providing strategies to 
						third-party clients on how to optimally leverage Liferay DXP to meet their functional requirements. 
						Multi-project experience using React/Freemarker/SCSS to create sleek and UX-friendly components 
						that meet design specifications."
					skills={['Java', 'JavaScript', 'React', 'OSGi', 'Liferay DXP', 'Jira', 'Github Actions']}
				/>
				<ExperienceCard
					href="https://www.thebluealliance.com/team/7157/2020"
					span="SEP 2017 - 2020"
					location="Brea, CA"
					title="FRC 7157 μBotics"
					subscript="Lead Programmer"
					description="Developed two competition bots with multi-threaded autonomous subroutines,
						closed-loop control (PID), and an award-winning vision pipeline.
						Integrated a suite of motor controllers and a Linux coprocessor (NVIDIA
						Jetson Nano) over a network-table based interface. Taught and led a team of 8 peers 
						throughout an intense twelve week sprint of competition, collaborated using Git source control."
					links={[
						{
							label: 'Creativity Award',
							href: 'https://www.firstinspires.org/resource-library/frc/awards-based-on-machine-creativity-innovation'
						}
					]}
					skills={['Java', 'Python', 'Git', 'Closed loop control', 'OpenCV', 'Ubuntu']}
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
				<div class="px-4 mb-8 lg:hidden">
					<span class="text-sm tracking-widest font-bold text-primary-50">PROJECTS</span>
				</div>
				<ExperienceCard
					href="https://github.com/dyoo47/svo-raytracer"
					image="img/colorblobs.webp"
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
					image="img/fearsha.webp"
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
					image="img/frc2020.webp"
					title="FRC 2019/2020 - Robot Code"
					description="Led the software development of two competition bots. Highlights include an award-winning vision pipeline,
						field position based shot calculation, and a PID controlled climb mechanism."
					links={[
						{ label: 'Github Repo', href: 'https://github.com/Mubotics7157' },
						{ label: '2019 Recap', href: 'https://www.youtube.com/watch?v=QehlMgzTxbY' },
						{ label: '2020 Recap', href: 'https://www.youtube.com/watch?v=Y51J-qdgaS8' }
					]}
					skills={['Java', 'Python', 'Git', 'Closed loop control', 'OpenCV', 'Ubuntu']}
				/>
				<ExperienceCard
					href="#"
					image="img/roguetactics.webp"
					title="Rogue Tactics"
					disableLink
					description="Multiplayer roguelike with a heavy emphasis on class specialization and item-based progression. Built using Godot."
					skills={['C#', 'Godot', 'Git', 'Multiplayer Networking', 'Godot Shaders']}
				/>
				<ExperienceCard
					href="https://klekky.itch.io/pool-party-showdown"
					image="img/poolparty.webp"
					title="Pool Party Showdown"
					description="Twin-stick beat 'em up game created in 7 days using Godot for the 2024 Pixel Game Jam. Officially judged as 5/5 stars
					in the Mechanics, Pixel Art, Design, and Theme categories."
					links={[
						{ label: 'Github Repo', href: 'https://github.com/dyoo47/pixeljam' },
						{ label: 'itch Page', href: 'https://klekky.itch.io/pool-party-showdown' },
						{
							label: 'Judge Ratings Sheet',
							href: 'https://docs.google.com/spreadsheets/d/1c0v334z37rz990xFaIXvo07nHIE3d_mf3eYmbpquw6c/edit?gid=0#gid=0'
						}
					]}
					skills={['C#', 'Godot', 'Git', 'Godot Shaders']}
				/>
				<ExperienceCard
					href="https://swordguy47.itch.io/tetris-mendacium"
					image="img/tetrismendacium.webp"
					title="Tetris Mendacium"
					description="Top-down puzzle game created in 7 days for the 2019 Community Game Jam. Developed with my brother in GameMaker Studio 2."
					links={[{ label: 'itch Page', href: 'https://swordguy47.itch.io/tetris-mendacium' }]}
					skills={['GameMaker Studio 2']}
				/>
				<ExperienceCard
					href="https://klekky.itch.io/"
					image="img/burger.webp"
					title="Ludum Dare Entries (LD 38, 39, 40, 42, 44)"
					description="A collection of browser games all created in under 72 hours for various Ludum Dare game jams."
					links={[
						{ label: 'Bitverse', href: 'https://klekky.itch.io/bitverse' },
						{ label: 'Hypersquare', href: 'https://klekky.itch.io/hypersquare-post-jam' },
						{ label: "Glutton's Heaven", href: 'https://klekky.itch.io/gluttons-heaven' },
						{ label: 'Geobreak', href: 'https://klekky.itch.io/geo' },
						{ label: 'goldenpixel', href: 'https://klekky.itch.io/goldenpixel' }
					]}
					skills={['Construct 2']}
				/>
			</section>
			<section>
				<p class="text-sm px-4">
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

					Deployed using
					<a
						href="https://www.netlify.com/?attr=homepage-modal"
						target="_blank"
						class="font-bold text-primary-50 hover:text-primary-300">Netlify.</a
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
