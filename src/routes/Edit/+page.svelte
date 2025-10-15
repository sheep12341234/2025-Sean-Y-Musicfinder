<script>
	import { goto } from '$app/navigation';
	import { redirect } from '@sveltejs/kit';

	let name = $state('');
	let email = $state('');
	let age = $state(undefined);


	function signUp() {
		let user = {
			name,
			email,
			age
		};

		localStorage.setItem('user', JSON.stringify(user));
		goto('/Home');
	}
</script>


<div class = "green-box">
  <button onclick={signUp} class="heading">Confirm</button>
  <br>
  <div class = "small">
    <div class = "pfp">
      <img class = "pic" src = "https://i.pinimg.com/236x/78/b5/48/78b548b33f3d83d4c682523194c9faac.jpg"/>
    </div>
  </div>
  <br>
  <br>
  <div class = "large">
    <input bind:value={name} class = "textbox" placeholder = "name" type = "text"/>
  <input bind:value={email} class = "textbox" placeholder = "email" type = "text"/>
    <input bind:value={age} class = "textbox" placeholder = "age" type = "number"/>
  </div>
  <div class = "discbox">
  </div>
</div>

<style>
    .green-box{
  height: 500px;
  width: 300px;
  background-color: lawngreen;
  border-radius: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 50px auto;
  flex-wrap: wrap;
}

.heading{
  font-size: 50px;
  font-weight: bold;
}

.small{
  border: 2px solid black;
  height: 100px;
  width: 250px;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.pfp{
  height: 50px;
  width: 50px;
}

.large{
  height: 200px;
  width: 250px;
  border: 2px solid black;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  
}

.textbox{
  width: 100px;
  height: 35px;
  border-radius: 15px;
  display: flex;
  justify-content: center;
}

.pic{
  border: 4px solid black;
  border-radius: 15px;
}

.discbox{
  font-size: 14px;
  width: 275px;
  display: flex;
  justify-content: center;
}
</style>