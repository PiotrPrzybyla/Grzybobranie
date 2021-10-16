<script>
	 import Nav from "./Components/Nav.svelte";
import Ratol from "./Components/Ratol.svelte";
import Poszkodowany from "./Components/Poszkodowany.svelte"
	 let activeSite = "main";
	 function showRatolSite(){
		activeSite = "ratol";
	 }
	 function backToMenu(){
		activeSite = "main"
	 }
	 function showPoszkodowanySite(){
		 activeSite = "poszkodowany"
	 }
</script>

<Nav/>
{#if activeSite == "main"}
<section class="pannels">
<div class="ratol" on:click={showRatolSite}>
	<h1>Panel Ratownika</h1>
</div>
<div class="pacjent" on:click={showPoszkodowanySite}>
	<h1>Panel Poszkodowanego</h1>
</div>
</section>
{:else if activeSite == "ratol"}
<h2 on:click={backToMenu}>Powrót</h2>
<Ratol/>
{:else if activeSite == "poszkodowany"}
<h2 on:click={backToMenu}>Powrót</h2>
<Poszkodowany/>
{/if}




<style>


	h1 {
		color: black;
		text-shadow: 2px 2px #ccc;
		text-transform: uppercase;
		font-size: 2.5em;
		font-weight: 500;
		margin: 0;
		display: block;
		/* background-color: rgba(150,150,150, .4); */
		width: 100%;
		line-height: 150%;
		/* padding: 10px; */

	}
	h2{
		/* text-align: right; */
		display: block;
		cursor: pointer;
		padding: 10px;
		position: absolute ;
		right: 0;
		top: 0;
	}
	section{
		width: 100%;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;


	}
	div{
		/* padding-top: 160px; */
		cursor: pointer;
		padding-bottom: 20px;
		width: 42vh;
		height: 42vh;
		text-align: center;
		border: 5px solid black;
		margin: 40px;
		/* z-index: auto; */
		border-radius: 30px;
		overflow: hidden;
		box-shadow: 5px 5px 10px black ;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
	}
	div.ratol{

		background-image: url('https://cdn.pixabay.com/photo/2016/09/16/19/12/ambulance-1674877_960_720.png');
		background-position: center;
		background-size: cover;
	}
	div.pacjent{
		background-image: url('https://cdn.pixabay.com/photo/2016/09/16/19/15/drug-1674890_960_720.png');
		background-position: center;
		background-size: cover;
	}
	
</style>