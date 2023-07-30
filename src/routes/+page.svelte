<script>
	import Fa from 'svelte-fa';
	import { faGithub, faLinkedin, faInstagram } from '@fortawesome/free-brands-svg-icons';
	import { faCode, faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import Button from '../components/Button.svelte';
	import Link from '../components/Link.svelte';
	import ExperienceCard from '../components/ExperienceCard.svelte';
	import EducationCard from '../components/EducationCard.svelte';

	function scrollTo() {
		window.scrollTo(0, 0);
	}
</script>

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
			<Button href="#"><Fa icon={faCode} /></Button>
			<Button href="#"><Fa icon={faGithub} /></Button>
			<Button href="#"><Fa icon={faLinkedin} /></Button>
			<Button href="#"><Fa icon={faInstagram} /></Button>
		</div>
	</div>
	<div class="text-slate-400 pb-20">
		<section id="about" class="pt-20">
			<div class="px-4">
				<span>
					I wrote my first ever line of code in grade school for a Minecraft mod. Since then, my
					curiosity has led me to explore diverse domains— web development, <a
						href="/"
						class="font-bold text-primary-50 hover:text-primary-300"
						>gamedev,
					</a>computer graphics, and robotics— just to name a few. I take great pleasure in
					immersing myself in novel concepts, readily embracing challenges and actively engaging in
					practical implementation.
					<br />
					<br />
					When I'm not coding I like to destress(?) by carrying my friends in
					<a href="/" class="font-bold text-primary-50 hover:text-primary-300">Valorant</a> or
					climbing at a
					<a href="/" class="font-bold text-primary-50 hover:text-primary-300">local gym.</a>
				</span>
			</div>
		</section>
		<div class="pt-28">
			<section id="experience" class="pb-28">
				<EducationCard
					href="#"
					description="Math-CS Major, 3.4 GPA"
					span="2020 - 2023"
					title="UC San Diego"
				/>
				<ExperienceCard
					href="#"
					span="2023 - present"
					location="Diamond Bar, CA"
					title="SWE Intern - Liferay, Inc."
					description="Full-time intern position in the Global Services consulting team, tasked
					with creating an out-facing portal for a government financial department.
					Designed and implemented 3 MVC web portlets under the OSGi specification
					as extensions of Liferay’s main open-source product (Liferay DXP),
					populated front-end JSP components with a mySQL database"
					skills={['React', 'OSGi', 'Liferay DXP', 'Jira', 'Github Actions']}
				/>
				<ExperienceCard
					href="#"
					span="SEP 2017 - 2020"
					location="Brea, CA"
					title="Lead Programmer - FRC 7157 μBotics"
					description="Developed a competition bot with multi-threaded autonomous subroutines,
closed-loop control (PID), and an award-winning vision pipeline
Integrated a suite of motor controllers and a Linux coprocessor (NVIDIA
Jetson Nano) over a network-table based interface
Taught and led a team of 8 peers throughout an intense twelve week sprint
of competition, collaborated using git source control"
					skills={['Java', 'Python', 'git', 'Closed loop control', 'OpenCV', 'Ubuntu']}
				/>
				<a href="/" class="group"
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
			<section id="projects">
				<ExperienceCard
					href="#"
					image="img/colorblobs.png"
					title="svo-raytracer"
					description="Realtime Java/LWJGL voxel path tracer based on the paper Efficient Sparse
					Voxel Octrees by Samuli Laine and Tero Karras. 2 bounces 1080p ~30fps, up to 2048^3 
					world size, implemented on GPU. Created a custom octree layout to maximize memory 
					coherency/efficiency and minimize ray traversal time"
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
					image="img/colorblobs.png"
					title="MineNet"
					description="Realtime Java/LWJGL voxel path tracer based on the paper Efficient Sparse
					Voxel Octrees by Samuli Laine and Tero Karras. 2 bounces 1080p ~30fps, up to 2048^3 
					world size, implemented on GPU. Created a custom octree layout to maximize memory 
					coherency/efficiency and minimize ray traversal time"
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
					image="img/colorblobs.png"
					title="Fearsha Frontend"
					description="Realtime Java/LWJGL voxel path tracer based on the paper Efficient Sparse
					Voxel Octrees by Samuli Laine and Tero Karras. 2 bounces 1080p ~30fps, up to 2048^3 
					world size, implemented on GPU. Created a custom octree layout to maximize memory 
					coherency/efficiency and minimize ray traversal time"
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
			</section>
		</div>
	</div>
</div>
