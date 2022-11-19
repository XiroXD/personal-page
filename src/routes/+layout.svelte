<script>
	import './styles.css';
</script>

<main>
	<slot />
</main>

<footer>Made By Creaperhunter#7718</footer>

<style>
	footer {
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
		width: 100%;
		height: 100%;

		min-height: 100vh;
	}
</style>
