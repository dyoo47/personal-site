<script>
	import Fa from 'svelte-fa';
	import { faGithub, faLinkedin, faInstagram } from '@fortawesome/free-brands-svg-icons';
	import { faCode } from '@fortawesome/free-solid-svg-icons';
	import Button from '../components/Button.svelte';
	import Link from '../components/Link.svelte';
	import ExperienceCard from '../components/ExperienceCard.svelte';
</script>

<div class="container px-10 lg:px-20 mx-auto grid align-top grid-cols-1 lg:grid-cols-2">
	<div class="lg:h-screen py-20 grid">
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
				<Link href="#">ABOUT</Link>
				<Link href="#">EXPERIENCE</Link>
				<Link href="#">PROJECTS</Link>
			</div>
		</div>
		<div class="self-end flex mt-5">
			<Button href="#"><Fa icon={faCode} /></Button>
			<Button href="#"><Fa icon={faGithub} /></Button>
			<Button href="#"><Fa icon={faLinkedin} /></Button>
			<Button href="#"><Fa icon={faInstagram} /></Button>
		</div>
	</div>
	<div class="py-20 text-slate-400">
		<div class="px-4">
			<span
				>One morning, when Gregor Samsa woke from troubled dreams, he found himself transformed in
				his bed into a horrible vermin. He lay on his armour-like back, and if he lifted his head a
				little he could see his brown belly, slightly domed and divided by arches into stiff
				sections. The bedding was hardly able to cover it and seemed ready to slide off any moment.
				His many legs, pitifully thin compared with the size of the rest of him, waved about
				helplessly as he looked.</span
			>
		</div>
		<div class="mt-20">
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
		</div>
	</div>
</div>
