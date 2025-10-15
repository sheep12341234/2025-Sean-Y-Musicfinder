<script>
	import { onMount } from 'svelte';

	let user = $state(undefined);

	onMount(() => {
		let u = localStorage.getItem('user');

		if (u !== null) {
			user = JSON.parse(u);
		}
	});
</script>

<div class="green-box">
	<div class="heading">Home</div>
	<hr />
	<div class="subheading">Good Morning!</div>
	<p>Age:  {user?.age}</p>
	<a class = "cont" href="/Contact">Contact me</a>
	<div class="subclass-circular">
		Favorites ^
		<div class="drop">
			<a href="https://www.youtube.com/watch?v=_hTsSthaI-4&list=RD_hTsSthaI-4&start_radio=1"
				>Lay Down</a
			>
		</div>
	</div>

	<br />
	<div class="subclass-circular">
		For You ^
		<div class="drop">
			<a href="https://www.youtube.com/watch?v=_hTsSthaI-4&list=RD_hTsSthaI-4&start_radio=1"
				>Lay Down</a
			>
		</div>
	</div>
	<br />
	<a href="/Browse" class="circle">Browse</a>
	<br />
	<a href="/Edit" class="Back">(Edit information)</a>
</div>

<style>
	.green-box {
		height: 500px;
		width: 300px;
		background-color: lawngreen;
		border-radius: 30px;
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 50px auto;
	}

	.heading {
		padding: 5px;
		font-size: 50px;
		font-weight: bold;
	}
	.subheading {
		font-size: 40px;
	}

	.subclass-circular {
		width: 175px;
		height: 50px;
		border: 5px solid black;
		border-radius: 35px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		font-size: 20px;
		transition-duration: 1s;
	}

	.drop {
		display: none;
	}

	.subclass-circular:hover {
		background-color: dodgerblue;
		height: 1000px;
	}

	.subclass-circular:hover .drop {
		display: block;
	}

	.circle {
		height: 100px;
		width: 100px;
		background-color: rgb(255, 166, 0);
		border-radius: 50px;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.circle:hover {
		background-color: gray;
	}

  .cont{

  }
  .cont:hover{
    color:blue;
  }
  .Back:hover{
    color: blue;
  }
</style>
