<script>
	function applySound(numero) {
		const audio = new Audio();
		audio.src = 'assets/sonidos/note' + numero + '.wav';
		audio.load();
		audio.play();
	}
</script>

<main>
	<nav class="navbar navbar-dark bg-primary text-center">
		Seven Notes Musical - SvelteApp
	</nav>

	<h3 class="text-center mt-1">Toca una nota</h3>

	<div class="row">
		<div class="col-lg-6">
			<div class="list-group">
				<div on:click={() => applySound(1)} class="list-group-item list-group-item-action" style="background-color: blue"></div>
				<div on:click={() => applySound(2)} class="list-group-item list-group-item-action" style="background-color: red"></div>
				<div on:click={() => applySound(3)} class="list-group-item list-group-item-action" style="background-color: orange"></div>
				<div on:click={() => applySound(4)} class="list-group-item list-group-item-action" style="background-color: yellow"></div>
				<div on:click={() => applySound(5)} class="list-group-item list-group-item-action" style="background-color: dark"></div>
				<div on:click={() => applySound(6)} class="list-group-item list-group-item-action" style="background-color: teal"></div>
				<div on:click={() => applySound(7)} class="list-group-item list-group-item-action" style="background-color: green"></div>
			</div>
		</div>
	</div>
</main>

<style>
	.list-group-item{
		cursor: pointer;
		height: 50px;
	}
	.row {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}
	.list-group-item:active {
		opacity: 0.9;	
	}
	main{
		background: #f2709c;  /* fallback for old browsers */
		background: -webkit-linear-gradient(to right, #ff9472, #f2709c);  /* Chrome 10-25, Safari 5.1-6 */
		background: linear-gradient(to right, #ff9472, #f2709c); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
	}
</style>