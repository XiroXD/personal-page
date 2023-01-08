<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let ready = false;
	onMount(() => (ready = true));
</script>

<svelte:head>
	<title>Creaperhunter | Home</title>
	<meta name="description" content="Just my personal page" />
</svelte:head>

{#if ready}
	<div class="main">
		<div>
			<h1 in:fly={{ duration: 850, y: 80 }}>Hi there 👋</h1>
			<h2 in:fly={{ delay: 1000, duration: 850, y: 100 }}>
				Im {#each 'Creaperhunter 👀' as char, i}
					<span in:fade={{ delay: 2000 + i * 120, duration: 800 }}>{char}</span>
				{/each}
			</h2>

			<h3 in:fly={{ delay: 3500, duration: 850, y: 80 }}>Fullstack web developer</h3>
			<h3 in:fly={{ delay: 3700, duration: 850, y: 80 }}>69420.host Co-Founder</h3>
			<h3 in:fly={{ delay: 3900, duration: 850, y: 80 }}>
				And proud founder of {#each 'Nothing...' as char, i}
					<span in:fade={{ delay: 4400 + i * 120, duration: 800 }}>{char}</span>
				{/each}
			</h3>

			<div class="socials">
				<a href="https://github.com/Creaperhunter" in:fly={{ delay: 5400, duration: 850, x: 100 }}>
					<i class="fa-brands fa-github" />
				</a>
				<a
					href="https://discords.com/bio/p/creaperhunter"
					in:fly={{ delay: 5600, duration: 850, x: 100 }}
					><i id="discord-icon" class="fa-brands fa-discord" /></a
				>
				<a
					id="guilded-icon"
					href="https://www.guilded.gg/u/creaperhunter"
					in:fly={{ delay: 5800, duration: 850, x: 100 }}
					><i class="fa-brands fa-guilded" />
				</a>
				<a
					href="https://steamcommunity.com/id/Creaperhunter/"
					in:fly={{ delay: 6000, duration: 850, x: 100 }}
				>
					<i class="fa-brands fa-steam" />
				</a>
			</div>
		</div>
		<div class="buttons">
			<a class="button" href="/projects" in:fly={{ duration: 850, x: 100 }}
				>{#each 'Projects' as char, i}
					<span in:fade={{ delay: 100 + i * 120, duration: 800 }}>{char}</span>
				{/each}</a
			>
			<a class="button" href="/contact" in:fly={{ duration: 850, x: 100, delay: 400 }}
				>{#each 'Contact' as char, i}
					<span in:fade={{ delay: 150 + i * 120, duration: 800 }}>{char}</span>
				{/each}</a
			>
		</div>
	</div>
{/if}

<style>
	.main {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		text-align: center;
		overflow: hidden;
	}
	@media (min-width: 768px) {
		.main {
			flex-direction: row;
			align-items: center;
			text-align: start;
			margin-left: 250px;
			margin-right: 250px;
			margin-bottom: 15em;
		}
	}
	.buttons {
		position: relative;
		display: flex;
		flex-direction: row;
		justify-content: center;
		gap: 20px;
		margin-top: 10px;
	}

	.socials {
		position: relative;
		display: flex;
		flex-direction: row;
		gap: 20px;
		font-size: 2rem;
		justify-content: center;
	}

	@media (min-width: 768px) {
		.socials {
			justify-content: flex-start;
		}
	}

	#discord-icon {
		color: #5865f2;
	}

	#guilded-icon {
		color: #f5c400;
	}
</style>
