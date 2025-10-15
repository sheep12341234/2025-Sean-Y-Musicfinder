<div class="green-box">
	<div class="heading">Browse</div>
	<hr />
	<div class="subheading">Relax!</div>
	<p>Age:</p>
	<br />
	<div class="subclass-circular">
		Christian ^
		<div class="drop">
			<a href="ss">Hip Hop</a>
		</div>
		<div class="drop">
			<a href="">Energetic</a>
		</div>
		<div class="drop">
			<a href="">Slow</a>
		</div>
		<div class="drop">
			<a href="">Jazz</a>
		</div>
	</div>

	<br />
	<div class="subclass-circular">
		Calm ^
		<div class="drop">
			<a href="">Study</a>
		</div>
		<div class="drop">
			<a href="">Sleep</a>
		</div>
	</div>
	<br />
	<a href="/Home" class="circle">Home</a>
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
		background-color: pink;
		border-radius: 50px;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.circle:hover {
		background-color: gray;
	}
</style>
