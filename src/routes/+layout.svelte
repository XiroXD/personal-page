<script>
	// import './styles.css';
	import seizure from '$lib/images/seizure.png';
</script>

<main>
	<div class="fimage">
		<img class="fitted" alt="siezure" src={seizure} />
	</div>
	<!-- <slot /> -->
</main>

<!-- <footer>Made By Creaperhunter#0001</footer> -->
<style>
	* {
		margin: 0;
		padding: 0;
	}
	.fimage {
		display: grid;
		height: 100%;
		justify-content: center;
	}
	.fitted {
		max-width: 100%;
		max-height: 100vh;
		margin: auto;
		border: none;
	}
	:global(body) {
		overflow: hidden;
		background-color: #000000;
	}
	/* footer {
		text-align: center;
		width: 100%;
		position: fixed;
		padding-bottom: 15px;
		bottom: 0;
		left: 0;
	}

	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		min-height: 100vh;
	} */
</style>
