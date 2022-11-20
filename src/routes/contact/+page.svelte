<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let ready = false;
	onMount(() => (ready = true));
</script>

{#if ready}
	<div class="main">
		<h1 in:fly={{ duration: 850, y: 80 }}>Contact</h1>
		<h2 in:fly={{ delay: 200, duration: 850, y: 80 }}>
			You can contact me at <a class="link" href="mailto:creaperhunter@hrzn.cool"
				>creaperhunter@hrzn.cool</a
			>
		</h2>
		<h3 in:fly={{ delay: 1200, duration: 850, y: 80 }}>Or the easier way...</h3>
		<div class="contact">
			<a href="https://discord.com/users/708370297094668388"
				><i
					id="discord-icon"
					class="fa-brands fa-discord"
					in:fly={{ delay: 1600, duration: 850, x: 100 }}
				/></a
			>
			<a id="guilded-icon" href="https://www.guilded.gg/u/creaperhunter"
				><i class="fa-brands fa-guilded" in:fly={{ delay: 1800, duration: 850, x: 100 }} /></a
			>
		</div>
		<div class="buttons" in:fly={{ duration: 850, y: 80, delay: 2000 }}>
			<a class="button" href="/"
				>{#each 'Return' as char, i}
					<span in:fade={{ delay: 2200 + i * 120, duration: 800 }}>{char}</span>
				{/each}</a
			>
		</div>
	</div>
{/if}

<style>
	a {
		position: relative;
		color: #fff;
	}

	h2 {
		font-size: 1.2rem !important;
	}

	.link {
		color: #fff;
		text-decoration: none;
		border-bottom: 3px solid #fff3;
	}

	.link:hover {
		border-bottom-color: #fff9;
	}

	.main {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-left: 10px;
		margin-right: 10px;
		margin-bottom: 15px;
		text-align: center;
	}

	@media (min-width: 778px) {
		.main {
			align-items: flex-start;
			margin-left: 250px;
			margin-right: 250px;
			margin-bottom: 15em;
		}
	}

	.contact {
		font-size: 2rem;
	}

	.buttons {
		position: relative;
		display: flex;
		flex-direction: row;
		gap: 30px;

		padding-top: 30px;
	}

	#discord-icon {
		color: #5865f2;
	}

	#guilded-icon {
		color: #f5c400;
	}
</style>
