<script>
	import { Tabs, TabList, TabPanel, Tab } from './tabs.js';
	let count = 0;
</script>


	<Tabs>
		<TabList>
			<Tab>one</Tab>
			<Tab>two</Tab>
			<Tab>three</Tab>
		</TabList>
	
		<TabPanel>
			<h2>First panel</h2>
			<main>
				<button on:click="{() => count += 1}">SEND KRAM</button>
			</main>
		</TabPanel>
	
		<TabPanel>
			<h2>Second panel</h2>
		</TabPanel>
	
		<TabPanel>
			<h2>Third panel</h2>
		</TabPanel>
	</Tabs>
	


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	button {
		background-color: white; 
  		border: 3px solid #555555;
		border-radius: 8px;
  		color: black;
  		padding: 15px 32px;
  		text-align: center;
  		text-decoration: none;
  		display: inline-block;
		position: absolute;
    	top: 50%;
  		font-size: 32px;
		box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>