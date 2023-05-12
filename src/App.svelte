<script>
	import Video from './lib/Video.svelte'
	import Info from './lib/Info.svelte'
	import './app.css'
	import { fade } from 'svelte/transition'
	let controller = new ScrollMagic.Controller()

	let bibliographyShown = false
	let experience = false

	if (window.location.pathname == '/references') {
		bibliographyShown = true
		experience = false
	} else if (window.location.pathname == '/') {
		bibliographyShown = false
		experience = false
	}

	window.addEventListener('popstate', () => {
		if (window.location.pathname == '/references') {
			bibliographyShown = true
			experience = false
		} else if (window.location.pathname == '/') {
			bibliographyShown = false
			experience = false
		}
	})
	function showBibliography() {
		bibliographyShown = true
		history.pushState({}, '', '/references')
	}
	function hideBibliography() {
		bibliographyShown = false
		history.pushState({}, '', '/')
	}
</script>

{#if !bibliographyShown && !experience}
	<main class="bg-black text-white" transition:fade>
		<Video bind:controller />
		<!--  -->
		<!-- Q1 -->
		<!--  -->
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">WHAT IS A GOLD RUSH?</h1>
				<p class="text-base max-w-xl">
					A gold rush occurs when there is a new and rapid income of people to a particular area due to newly
					discovered gold. People would flock over to the sites of newly discovered gold to try their luck in
					hopes of making a great fortune, potentially leaving behind their whole family and just going by
					themselves. Finding gold was never guaranteed; miners would head down to the diggings unsure if they
					would make a new fortune or if it would be another day of not finding anything.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 1: 'Prospectors' by ST Gill, 1865.</h1>
				</div>
				<img
					src="https://www.nma.gov.au/__data/assets/image/0010/547228/MA44137263-prospecting-1200w.jpg"
					alt="Prospectors by ST Gill"
					width="600px"
					height="300px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div class="relative">
				<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 2: 'Gold Washing' by George French Angas, 1851.</h1>
				</div>
				<img
					src="https://www.nma.gov.au/__data/assets/image/0007/567070/MA37181365-Gold-washing-1200w.jpg"
					alt="Gold Washing by George French Angas"
					width="600px"
					height="300px"
				/>
			</div>
			<div>
				<h1 class="text-4xl font-display">WHAT IS A GOLD RUSH?</h1>
				<p class="text-base max-w-xl">
					Gold rushes occurred across the world, with major rushes happening in the United States, Australia,
					Canada and South Africa. Multiple thousands of people would head to areas of gold discovery, and up
					to 250,000 travelled to the United States for a gold rush, and Australia’s population quadrupled
					from 430,000 people to 1.7 million when gold was discovered across the country. The migration of
					people was greatly affected during that time period, with people travelling across the world and
					settling in the areas of gold.
				</p>
			</div>
		</Info>
		<!--  -->
		<!-- Q2 -->
		<!--  -->
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">HOW DID THE BALLARAT GOLD RUSH START?</h1>
				<p class="text-base max-w-xl">
					In August 1851, John Dunlop and James Regan left the gold field at Buninyong when it was overrun
					with many people looking for gold after news got out about the discovery of gold in that region.
					They moved out to Ballarat where they used gold panning and cradles to help them find gold as shown
					on the right. They discovered a much richer digging on the 21st of August 1851. However, a newspaper
					reporter had followed them to the diggings and had reported on their finds and, as a result, they
					only had the goldfield to themselves for a week before other prospectors came in. Within a year,
					more than 20,000 diggers were trying their luck in the mine shafts of Ballarat.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 3: 'An Australian Gold Diggings' by Edwin Stockqueler, 1855.</h1>
				</div>
				<img
					src="https://upload.wikimedia.org/wikipedia/commons/f/ff/An_Australian_Gold_Diggings.jpg"
					alt="An Australian Gold Diggings by Edwin Stockqueler"
					width="600px"
					height="300px"
				/>
			</div>
		</Info>
		<!--  -->
		<!-- Q3 -->
		<!--  -->
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display text-right">WHO CAME TO BALLARAT?</h1>
				<p class="text-base max-w-3xl text-right">
					Many people across the world came to Victoria for the gold rush. Some of the people travelled within
					Australia, from other places to Ballarat for the gold rush. However, most of the prospectors would
					come from places overseas such as Britain, the United States, Germany, and Poland. Australia also
					saw a large influx of Chinese emigrants, which was the largest number of non-European settlers to
					come to Australia for the gold rush. Many people abandoned their stable jobs in order to test their
					luck in the mines, and there was a shortage of workers for this reason.
				</p>
			</div>
		</Info>
		<!--  -->
		<!-- Q4 -->
		<!--  -->
		<Info bind:controller>
			<div class="relative">
				<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 4: 1850s Sailing Clipper by Bill Wood.</h1>
				</div>
				<img
					src="https://museumsvictoria.com.au/media/6928/000010127.jpg"
					alt="1850s Sailing Clipper by Bill Wood"
					width="500px"
					height="200px"
				/>
			</div>
			<div>
				<h1 class="text-4xl font-display">SHIPS: GETTING TO AUSTRALIA</h1>
				<p class="text-base max-w-xl">
					In the early 1800s, it was common for people to arrive in Australia by sailboat, which would be a
					long and dangerous trip. It would last for around 4 months, however, travelling on a clipper would
					half this time. Later on, auxiliary steamer ships made it possible to travel with both steam and
					sail, but this would be an unlikely trip as steam engines were too inefficient to travel the
					distance required to get to Australia. Despite this, in 1852, the first steamship made its way to
					Australia. It was mostly powered by its steam engine but it was equipped with backup sails as they
					usually ran out of coal. Steamships were usually better as they were made of iron and provided
					better comfort compared to wooden sailboats.
				</p>
			</div>
		</Info>
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">NAVIGATION: GETTING TO AUSTRALIA</h1>
				<p class="text-base max-w-xl">
					Navigating to Australia was a complex and challenging task, requiring great skill from a captain in
					order to arrive safely. Multiple tools were used to get to Australia, including the telescope,
					marine compass, ship’s log, and sextant. To get to Australia, most ships would follow along the
					‘Great Circle’ route as it allowed them to get there faster. They would travel far below the Cape of
					Good Hope in order to enter between 40 and 50 degrees south as it had strong winds getting them
					towards the direction of Australia. However, this route provoked many risks, from drifting icebergs
					to the wild seas created by frequent storms. The slightest of error in navigation along this route
					could lead to a disaster, and the number of deaths increased by taking this route, compared to the
					traditional way of getting to Australia. The artwork on the right depicts the tradgedy of the
					shipwrecks that occured along the great circle route. The wild seas are evident, tearing apart the
					ship and putting the passenger's lives at great risk. This was the unfortuneate reality of most
					ships taking this route to Australia.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 5: The wreck of the 'Loch Ard', 1878.</h1>
				</div>
				<img
					src="https://museumsvictoria.com.au/media/6933/000010025-loch-ard.jpg"
					alt="The wreck of the 'Loch Ard' in 1878"
					width="800px"
					height="600px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div class="relative">
				<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 6: The 'Great Circle' route used to get to Australia.</h1>
				</div>
				<img
					src="https://museumsvictoria.com.au/media/6931/000017841.jpg"
					alt="The 'Great Circle' route used to get to Australia"
					width="900px"
					height="700px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">LIFE ON BOARD: GETTING TO AUSTRALIA</h1>
				<p class="text-base max-w-3xl">
					Most people making their way to Australia were unfamilar with sea travel, and the travel to
					Australia involved navigating through some of the wildest oceans. As seen in the image below, living
					quaters were quite cramped in 'steerage' class, where most passengers were travelling. This would
					support the spread of disease and sickness, making an unpleasant journey. Seasickness was common,
					especially among those who were unaccustomed to sea travel. As a result of this, death at sea was
					very common, with 1 in 5 children and 1 in 60 adults not being able to survive the journey.
				</p>
				<p class="text-base max-w-3xl mt-3">
					Water was kept in barrels, but they were left open where algae would grow and rats and mice would
					fall in making the water stale after just a few months. Food was kept in barrels that were opened
					when needed by the cooks, which were usually fitted with lids. However, the cooks would often leave
					the lids of the barrels overnight letting in rats and mice to raid the storage. Hygiene was no
					better, with most ships only providing basic toilet and cleaning facilities, but most passengers
					just used the upper decks as open-air toilets. The waste from toilets was stored in the bottom of
					the ship, creating a worse experience for people in steerage. Simple practices of hygiene were
					unknown at the time, and outbreaks of multiple diseases happened frequently on ships.
				</p>
			</div>
		</Info>
		<Info bind:controller>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 7: 'Emigrants at dinner' by unknown artist, 1844.</h1>
				</div>
				<img
					src="https://museumsvictoria.com.au/media/6936/000009990.jpg"
					alt="'Emigrants at dinner' by unknown artist"
					width="800px"
					height="600px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">EXPERIENCE: GETTING TO AUSTRALIA</h1>
				<p class="text-base max-w-xl">
					Ally Heathcote was a passenger from England to Melbourne on the ‘SS Northumberland’. Heathcote
					experienced a “storm” upon her journey to Australia, where she was “wondering how long [it] would
					last” wanting “protection when crash went something on deck”. Water came in “over the decks and down
					into the cabin[s]”, and people would “rush out of their cabins looking terrified” as they flooded in
					second class. A few days earlier, she “starved to death almost” as their “ships rolls [them] about …
					every meal time”. They had to “hold on to the tables and seats and keep [their] cups from wandering
					all over the cabin” as the seas were so violent. During the night, they were “constantly on the
					move, first one side [of the bed] then the other”, however, they “fared better than the second cabin
					passengers, as they have the engine right in the midst of them” making for a hot and noisy journey.
					Heathcote demonstrates an example of life on board, and the horrible conditions those experienced
					travelling to Australia.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 8: Ally Heathcote's diary, 1874.</h1>
				</div>
				<img
					src="https://collections.museumsvictoria.com.au/content/media/32/296632-small.jpg"
					alt="Ally Heathcotes Diary"
					width="500px"
					height="300px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div class="relative">
				<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 9: An artwork of Chinese emigrants, 1857.</h1>
				</div>
				<img
					src="https://museumsvictoria.com.au/media/6926/000000357.jpg"
					alt="'A Flood of Celestial Light pouring in upon the Diggings' reproduced from Melbourne Punch"
					width="600px"
					height="400px"
				/>
			</div>
			<div>
				<h1 class="text-4xl font-display">THE VICTORIAN POLL TAX</h1>
				<p class="text-base max-w-xl">
					Chinese miners in Ballarat faced a difficult time in the gold fields. With a language barrier and
					differentiators in dress and appearance, Chinese miners were more likely to face discrimination in
					the diggings. Furthermore, Chinese miners would go through the abandoned mines the Europeans left
					behind, often finding gold that was missed, which made them a subject of discrimination. Eventually,
					the Victorian colony passed an act that restricted the entry of Chinese emigrants. The act entitled
					ships to only have 1 Chinese person for 10 tonnes of the ship’s cargo. On top of this, ships were
					required to pay £10 for each Chinese migrant.
				</p>
				<p class="text-base max-w-xl mt-3">
					To avoid this, the Chinese emigrants often travelled to South Australia instead and would walk 500
					kilometres over to Ballarat carrying their belongings. The image on the left shows the Chinese
					miners making their journey from Adelaide to the goldfields in Victoria. There is a large group of
					them, all carrying their belongings meaning that they most likely just got off a ship and have
					started the journey in a big group. There is some evidence that this act influenced the creation of
					the White Australia Policy in 1901, which restricted non-European immigrants from coming into the
					country.
				</p>
			</div>
		</Info>
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">GOLD LICENSE</h1>
				<p class="text-base max-w-xl">
					During the rapid increase in population as the Victorian gold rush became more popular, it proved
					more difficult for the government to get funding and to support the hundred-thousands more people
					migrating to Australia. To try and slow down the number of people coming in, and increase government
					funding, a 2-pound per three months license was implemented (worth around $344.54 in today’s
					currency). Police regularly ran ‘licence hunts’ on the miners, however, the miners claim the police
					were accepting bribes and imprisoning people without going through court. This created conflict
					between the miners and the government in the goldfields.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 10: A gold license used in Ballarat.</h1>
				</div>
				<img
					src="https://www.oldtreasurybuilding.org.au/wp-content/uploads/2018/06/Gold-Licence-ed-sm.jpg"
					alt="A gold license used in Ballarat"
					width="600px"
					height="400px"
				/>
			</div>
		</Info>
		<Info bind:controller>
			<div class="relative">
				<div
					class="absolute -top-5 -left-5 2xl:-left-16 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md"
				>
					<h1 class="text-base">
						Source 11: 'Swearing Allegiance to the Southern Cross' by Charles A Doudiet, 1854.
					</h1>
				</div>
				<img
					src="https://www.nma.gov.au/__data/assets/image/0019/548011/MA23237597-Allegiance-1200w.jpg"
					alt="'Swearing Allegiance to the Southern Cross' by Charles A Doudiet"
					width="600px"
					height="400px"
				/>
			</div>
			<div>
				<h1 class="text-4xl font-display">EUREKA REBELLION</h1>
				<p class="text-base max-w-xl">
					Another discrepancy between the government and the miners led to the police searching through all
					the miner’s tents checking for the gold license. The miners were fed up with the police and gathered
					at Bakery Hill to build a stockade made with wood from mineshafts. Over the following days, the
					miners practised military drills and prepared for a possible fight. Eventually, on Sunday the 3rd of
					December 1854, the police and the army were commanded to destroy the stockade at 4 am in the
					morning. The prior night, many miners did not think anyone would come, and in turn, the total number
					of people dropped from 1000 people to only 100 people, making for a much weaker army during the
					fight. As a result of this, the whole conflict only lasted 15 minutes and the soldiers (police) came
					out victorious. This event became known as the ‘Eureka Rebellion’ or the ‘Eureka Stockade’. The
					Victorian Government understood the miner’s frustration and removed the gold license replacing it
					with a more affordable ‘Miner’s Right’, costing only 1 pound (worth around $172.27 in today’s
					currency) per year.
				</p>
			</div>
		</Info>
		<Info bind:controller>
			<div>
				<h1 class="text-4xl font-display">THE WELCOME NUGGET</h1>
				<p class="text-base max-w-xl">
					The “Welcome Nugget” was the largest golden nugget (at that time) discovered during the evening of
					the 9th of June, 1858. A Cornish miner John Deason and his partner Richard Oates initially found the
					nugget, then excitedly called in more mine workers to help them take out the nugget making a total
					of 22 miners. It weighed 69 kilograms and was over 99% pure gold, giving the first two miners a
					fortune of £10,000 to split (worth approximately $1,722,680.06 in today’s currency) when it was
					bought by London’s Royal Mint and turned into coins. The discovery of the nugget caused a small
					uproar, as the gold mining occurring at Ballarat had slowed down, with many people believing there
					was nothing left. However, the Welcome Nugget proved them wrong and sparked interest again in the
					Ballarat diggings.
				</p>
			</div>
			<div class="relative">
				<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
					<h1 class="text-base">Source 12: Replica of the Welcome Nugget.</h1>
				</div>
				<img
					src="https://www.sovereignhill.com.au/_next/image/?url=https://cdn.sovereignhill.com.au/_fullFit/7658/Welcome-Nugget-Replica_Landscape.webp&w=1080&q=75"
					alt="Replica of the Welcome Nugget"
					width="600px"
					height="400px"
				/>
			</div>
		</Info>

		<Info bind:controller>
			<div class="bg-amber-600 p-5 rounded-lg max-w-2xl">
				<h1 class="text-4xl font-display">THANK YOU</h1>
				<p class="text-base">
					This is a website created by a student for a school project, covering the migration and immigration
					to Ballarat as a result of the gold rush. I hope you enjoyed reading about the fascinating history
					of Ballarat's gold rush, and the events that happened during the time.
				</p>
				<button class="bg-amber-500 p-2 px-3 rounded-lg hover:underline my-5" on:click={showBibliography}
					>View references list →</button
				>
				<p class="text-base mt-5">
					Made with Svelte, Tailwindcss and ScrollMagic. Hosted on Vercel. <a
						href="https://github.com/TheCoder76-Codes/gold"
						class="hover:underline">Source code here on Github.</a
					>
					Created by Max May (TheCoder76). Last updated on 12/05/2023. This material is licensed under the CC-BY-SA
					license. For more information, visit
					<a
						href="https://creativecommons.org/licenses/by-sa/4.0/"
						target="_blank"
						rel="noreferrer"
						class="hover:underline">this website.</a
					>
				</p>
			</div>
		</Info>
		<div class="bg-black h-96">
			<p class="text-6xl text-black cursor-default">This is a separator container, for Scrollmagic. Wow!</p>
		</div>
		<div class="bg-black h-40">
			<p class="text-6xl text-black cursor-default">This is a separator container, for Scrollmagic. Wow!</p>
		</div>
	</main>
{:else if bibliographyShown}
	<div class="p-5 bg-black text-white min-h-screen refernces" transition:fade>
		<h1 class="text-4xl font-display">References</h1>
		<p class="text-base max-w-xl">
			Ally Heathcote. (1874). Diary – Ally Heatcote, England to Melbourne, Victoria, Onboard ‘SS Northumberland’,
			1874. Museums Victoria Collections.
			<a href="https://collections.museumsvictoria.com.au/items/272753"
				>https://collections.museumsvictoria.com.au/items/272753</a
			>
		</p>
		<p class="text-base max-w-xl">
			Britannica, T. Editors of Encyclopaedia (2021, August 12). Gold rush. Encyclopedia Britannica.
			<a href="https://www.britannica.com/event/gold-rush">https://www.britannica.com/event/gold-rush</a>
		</p>
		<p class="text-base max-w-xl">
			Curator, Old Treasury Building. (n.d.). The Humble Petition of the Chinese Storekeepers. Old Treasury
			Building.
			<a href="https://www.oldtreasurybuilding.org.au/the-humble-petition-of-the-chinese-storekeepers/"
				>https://www.oldtreasurybuilding.org.au/the-humble-petition-of-the-chinese-storekeepers/</a
			>
		</p>
		<p class="text-base max-w-xl">
			Curator, Old Treasury Building. (n.d.). Welcome Stranger Replica Nugget.
			<a href="https://www.oldtreasurybuilding.org.au/welcome-stranger-replica-nugget/"
				>https://www.oldtreasurybuilding.org.au/welcome-stranger-replica-nugget/</a
			>
		</p>
		<p class="text-base max-w-xl">
			Documenting Democracy. (n.d.). Chinese Immigration Act 1855 (Vic).
			<a href="https://www.foundingdocs.gov.au/item-sdid-18.html"
				>https://www.foundingdocs.gov.au/item-sdid-18.html</a
			>
		</p>
		<p class="text-base max-w-xl">
			Immigration Museum. (n.d.) Journeys to Australia.
			<a href="https://museumsvictoria.com.au/immigrationmuseum/resources/journeys-to-australia/"
				>https://museumsvictoria.com.au/immigrationmuseum/resources/journeys-to-australia/</a
			>
		</p>
		<p class="text-base max-w-xl">
			Monument Australia. (n.d.). Poverty Point Gold Discovery.
			<a href="https://www.monumentaustralia.org.au/display/30207-poverty-point-gold-discovery"
				>https://www.monumentaustralia.org.au/display/30207-poverty-point-gold-discovery</a
			>
		</p>
		<p class="text-base max-w-xl">
			National Geographic Society. (n.d.) Australian Gold Rush Begins. National Geographic.
			<a href="https://education.nationalgeographic.org/resource/australian-gold-rush-begins/"
				>https://education.nationalgeographic.org/resource/australian-gold-rush-begins/</a
			>
		</p>
		<p class="text-base max-w-xl">
			National Museum Australia. (2022, September 21). Defining Moments: Eureka Stockade.
			<a href="https://www.nma.gov.au/defining-moments/resources/eureka-stockade"
				>https://www.nma.gov.au/defining-moments/resources/eureka-stockade</a
			>
		</p>
		<p class="text-base max-w-xl">
			National Museum Australia. (2023, February 8). Defining Moments: Gold Rushes.
			<a href="https://www.nma.gov.au/defining-moments/resources/gold-rushes"
				>https://www.nma.gov.au/defining-moments/resources/gold-rushes</a
			>
		</p>
		<p class="text-base max-w-xl">
			National Museum Australia. (n.d.) Victorian Goldfields: Victorian goldfields for kids.
			<a href="https://www.nma.gov.au/learn/kspace/victorian-goldfields-1854/kids"
				>https://www.nma.gov.au/learn/kspace/victorian-goldfields-1854/kids</a
			>
		</p>
		<p class="text-base max-w-xl">
			Pamie Fung. (2015, June 12). The Significance of the First Anti-Chinese Legislation in Australia. Peril.
			<a href="https://peril.com.au/topics/politics/anti-chinese-legislation-in-australia/"
				>https://peril.com.au/topics/politics/anti-chinese-legislation-in-australia/</a
			>
		</p>
		<p class="text-base max-w-xl">
			Reserve Bank of Australia. (n.d.). Pre-Decimal Inflation Calculator.
			<a href="https://www.rba.gov.au/calculator/annualPreDecimal.html"
				>https://www.rba.gov.au/calculator/annualPreDecimal.html</a
			>
		</p>
		<p class="text-base max-w-xl">
			SBS Gold. (n.d.). Interactive Map.
			<a href="https://www.sbs.com.au/gold/map/">https://www.sbs.com.au/gold/map/</a>
		</p>
		<p class="text-base max-w-xl">
			SBS Gold. (n.d.). Rush for Gold.
			<a href="https://www.sbs.com.au/gold/rush-for-gold/">https://www.sbs.com.au/gold/rush-for-gold/</a>
		</p>
		<p class="text-base max-w-xl">
			Sovereign Hill. (2021, June 8th). The Story of the Welcome Nugget.
			<a href="https://sovereignhill.com.au/welcome-nugget">https://sovereignhill.com.au/welcome-nugget</a>
		</p>
		<button class="bg-amber-500 p-2 px-3 rounded-lg hover:underline" on:click={hideBibliography}>Go back →</button>
	</div>
{/if}
