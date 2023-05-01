<script>
	import '../tailwind.css';
	import './styles.css';
</script>

<main class="flex flex-col justify-center min-h-screen">
	<slot />
</main>

<footer>Made With 💖 By Xiro#0001</footer>

<style>
	footer {
		text-align: center;
		width: 100%;
		position: fixed;
		padding-bottom: 15px;
		bottom: 0;
		left: 0;
	}
</style>
