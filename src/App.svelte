<script>
	import { Tabs, TabList, TabPanel, Tab } from './tabs.js';
	import { user } from "./store.js";
	
</script>


	<Tabs>
		<TabList>
			<Tab>Send en kram</Tab>
			<Tab>Jeg er sundhedspersonale</Tab>
			<Tab>Live Kram Feed</Tab>
		</TabList>
	
		<TabPanel>
			<main>
				<div class="wrapper">
					<button>SEND KRAM</button>
				</div>
				
			</main>
		</TabPanel>
	
		<TabPanel>
			<h1>Jeg vil gerne fa en kram</h1>
			<form class="content">
			<label>Navn</label>
				<input type="text" bind:value={$user.name} />
			<label>Telefon</label>
				<input type="text" bind:value={$user.phone} />

				<button>Send</button>
			</form>
			<p>
			{JSON.stringify($user, 0, 2)}
			</p>
		</TabPanel>
	
		<TabPanel>
			<h2>Live Kram Feed!</h2>
		</TabPanel>
	</Tabs>
	


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	.wrapper {
    text-align: center;
	display: block;
	top: 50%;
	right: 50%;
	}

	button {
		display: block;
		margin: 0 auto;
		background-color: white; 
  		border: 3px solid #555555;
		border-radius: 8px;
  		color: black;
  		padding: 15px 32px;
  		text-align: center;
  		text-decoration: none;   	
  		font-size: 24px;
		box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
	}

	.content {
    display: grid;
    grid-template-columns: 20% 80%;
    grid-column-gap: 10px;
  	}
	
	input {
		width: 50%;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>