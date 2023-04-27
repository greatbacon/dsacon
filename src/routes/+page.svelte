<script lang="ts">
	//TODO make content an array & put seperate items on new lines
	//TODO make an enum for phase of timeline (resolution|at-large;chapter;NPC elections|proposal amendments|registration|convention)
	//TODO use enum to style dot & background
	//TODO move to own route(?)


	import Message from '@feltjs/felt-ui/Message.svelte';

	import {
		Timeline,
		TimelineItem,
		TimelineSeparator,
		TimelineDot,
		TimelineConnector,
		TimelineContent,
		TimelineOppositeContent
	} from 'svelte-vertical-timeline';

	const options = [
		{date: 'February 20', content:'Submissions open for Resolutions & Amendments. This is also the Deadline to be a member in good standing to sign onto proposals.'},
		{date: 'February 28' ,content:'Deadline to request to be considered an at-large member before Convention'},
		{date: 'March 17' ,content:'Delegate apportionment finalized and sent to chapters'},
		{date: 'April 4' ,content:'Nominations open for at-large delegates. Elections begin for chapter delegates. Nominations open for National Political Committee (NPC) candidates.'},
		{date: 'April 15' ,content:'Submissions open for amendments to submitted proposals.'},
		{date: '🌹', content: 'WE ARE HERE!'},
		{date: 'April 28' ,content:'Submission period for proposals are closed.'},
		{date: 'May 4' ,content:'Nominations close for at-large delegates.'},
		{date: 'May 13' ,content:'Registraion and scholarship processes open. Early-bird registration starts.'},
		{date: 'May 18' ,content:'At-large delegate elections open.'},
		{date: 'June 6' ,content:'Election results for chapter delegates must be reported. At-large delegate elections end.'},
		{date: 'June 14' ,content:'Nominations close for NPC candidates.  Early-bird registration closes.'},
		{date: 'June 15' ,content:'Regular registration perioid begins.'},
		{date: 'June 28' ,content:'Submission period for amendments to proposals closes.'},
		{date: 'June 30' ,content:'Compendium of proposals & NPC candidates released.'},
		{date: 'July 13' ,content:'Registration closes.'},
		{date: 'July 14' ,content:'NPC candidate forum held.'},
		{date: 'July 24' ,content:'Final compendium of proposals and NPC candidates released.  Temporary roster of elected chapter and at-large delegates released'},
		{date: 'July 26' ,content:'Deadline for credentials challenges.'},
		{date: 'August 4' ,content:'DAY 1 of CONVENTION'},
		{date: 'August 5' ,content:'DAY 2 of CONVENTION'},
		{date: 'August 6' ,content:'DAY 3 of CONVENTION'},
	];
</script>

<main class="markup column">
	<section>
		<header class="centered-hz">
			<h1>DSA CONVENTION INFO 2023</h1>
		</header>
		<Message icon="🌹">
				TIMELINE | DELEGATES | CAUCUSES | PROPOSALS | ELECTIONS | NEWS
			</Message
		>
	</section>	
</main>

<Timeline position="left" style={"border: solid 1px #dbdbdb; padding: 50px 0; border-radius: 2%;"}>
	{#each options as option}
		<TimelineItem>
			<TimelineOppositeContent slot="opposite-content">
				<p>{option.content}</p>
			</TimelineOppositeContent>
			<TimelineSeparator>
				<TimelineDot style={'background-color: #7CD5E2;'}/>				
				<TimelineConnector />
			</TimelineSeparator>
			<TimelineContent>
				<h3>{option.date}</h3>
			</TimelineContent>
		</TimelineItem>
	{/each}
</Timeline>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0 auto;
		padding-bottom: 1%;
	}
	h1 {
		text-align: center;
	}

	h3 {
		letter-spacing: 1.5px;
		margin: 0;
		padding: 0;
	}
	
	p {
		letter-spacing: 1.5px;
		margin: 0;
		color: grey;
		width: 40%;
	}
</style>
