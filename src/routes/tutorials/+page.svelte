<script lang="ts">
	const tutorials = [
		{
			id: 1,
			title: 'Introduction to Python',
			description:
				'Learn the basics of Python programming, including syntax, variables, and basic operations.',
			author: 'Richard Price',
			difficulty: 'Beginner'
		},
		{
			id: 2,
			title: 'Web Development with HTML and CSS',
			description: "A beginner's guide to building web pages using HTML and CSS.",
			author: 'Richard Price',
			difficulty: 'Beginner'
		},
		{
			id: 3,
			title: 'Advanced JavaScript Techniques',
			description:
				'Explore advanced concepts in JavaScript including closures, prototypes, and async programming.',
			author: 'Richard Price',
			difficulty: 'Advanced'
		},
		{
			id: 4,
			title: 'Introduction to React',
			description:
				'Get started with React, a popular JavaScript library for building user interfaces.',
			author: 'Richard Price',
			difficulty: 'Intermediate'
		},
		{
			id: 5,
			title: 'Building RESTful APIs with Node.js',
			description: 'Learn how to create RESTful APIs using Node.js and Express.',
			author: 'Richard Price',
			difficulty: 'Intermediate'
		},
		{
			id: 6,
			title: 'Data Analysis with Python',
			description:
				'Discover how to use Python for data analysis, including libraries like Pandas and NumPy.',
			author: 'Richard Price',
			difficulty: 'Intermediate'
		}
	];
</script>

<div class="w-full text-token grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
	{#each Object.entries(tutorials) as [id, entry]}
		<a class="card bg-initial card-hover overflow-hidden" href="/tutorials/{entry.title}"
			><header>
				<img
					src="https://source.unsplash.com/random/400×175/?{entry.title}"
					class="bg-black/50 w-full aspect-[21/9]"
					alt="Post"
				/>
			</header>
			<div class="p-4 space-y-4">
				<h6 class="h6" data-toc-ignore="">Announcements</h6>
				<h3 class="h3" data-toc-ignore="">{entry.title}</h3>
				<article>
					<p>
						{entry.description}
					</p>
				</article>
			</div>
			<hr class="opacity-50" />
			<footer class="p-4 flex justify-start items-center space-x-4">
				<figure
					class="avatar flex aspect-square text-surface-50 font-semibold justify-center items-center overflow-hidden isolate bg-surface-400-500-token w-8 rounded-full"
					data-testid="avatar"
				>
					<img
						class="avatar-image w-full h-full object-cover"
						src="https://images.unsplash.com/photo-1617296538902-887900d9b592?ixid=M3w0Njc5ODF8MHwxfGFsbHx8fHx8fHx8fDE2ODc5NzExMDB8&amp;ixlib=rb-4.0.3&amp;w=32&amp;h=32&amp;auto=format&amp;fit=crop"
						alt=""
						style=""
					/>
				</figure>
				<div class="flex-auto flex justify-between items-center">
					<h6 class="font-bold" data-toc-ignore="">By {entry.author}</h6>
					<small>On 18/12/2023</small>
				</div>
			</footer>
			<small>{entry.difficulty}</small>
		</a>
	{/each}
</div>
