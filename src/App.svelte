<script>
	import { Tabs, TabList, TabPanel, Tab } from './tabs.js';
	import { user } from "./store.js";

</script>

<Tabs>
	<TabList>
		<Tab>Send kram</Tab>
		<Tab>Modtag kram</Tab>
		<Tab>Live Kram Feed</Tab>
	</TabList>

	<TabPanel>
		<main>
			<div class="wrapper">
				<button class="main_button">SEND ET KRAM</button>
			</div>

		</main>
	</TabPanel>

	<TabPanel>
		<h1>Send kram til mig</h1>
		<form class="content">
			<label>Telefon</label>
			<input type="text" bind:value={$user.phone} />

			<button class="signup_button">Gem</button>
		</form>
	</TabPanel>

	<TabPanel>
		<h2>Live Kram Feed!</h2>
		<h5>To do</h5>
	</TabPanel>
</Tabs>



<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 1200px) {
		main {
			max-width: 240px;
		}
	}

	.main_button {
		display: block;
		cursor: pointer;
		margin: 10% auto 5%;
		background-color: white;
		border: 3px solid #555555;
		border-radius: 8px;
		color: black;
		padding: 15px 32px;
		text-align: center;
		text-decoration: none;
		font-size: 5vw;
		box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
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