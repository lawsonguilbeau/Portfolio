<!-- src/lib/components/Experience.svelte -->
<script>
	const experiences = [
		{
			company: "Ena Pragma Consulting",
			role: "Web Development Intern",
			period: "2026",
			description:
				"Developed responsive full-stack features using React, Node.js, and PostgreSQL. Integrated REST APIs, designed database models with Prisma, and collaborated closely on client deliverables."
		}
	];
</script>

<div class="flex flex-col gap-10 max-w-[800px] mx-auto w-full py-8">
	<h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
		Work <span class="text-cyan-400">Experience</span>
	</h5>
	<div class="flex flex-col gap-6">
		{#each experiences as exp}
			<div
				class="border border-slate-800 p-6 rounded-lg bg-slate-900/60 flex flex-col gap-3 text-left"
			>
				<div class="flex justify-between items-center flex-wrap gap-2">
					<h3 class="text-xl font-semibold text-white">
						{exp.role} <span class="text-cyan-400">@ {exp.company}</span>
					</h3>
					<span class="text-sm text-slate-400">{exp.period}</span>
				</div>
				<p class="text-slate-300 text-sm sm:text-base leading-relaxed">{exp.description}</p>
			</div>
		{/each}
	</div>
</div>
