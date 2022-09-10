<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	export async function load({ fetch }) {
		const res = await fetch(`/posts.json`);
		const posts = await res.json();

		return {
			props: {
				posts
			}
		};
	}
</script>

<script>
	import Seo from '$lib/Seo.svelte';
	import BlogSummary from '$lib/BlogSummary.svelte';
	import { variables } from '$lib/variables';
	export let posts;

	const postsToShow = 3;
	$: blogPosts = posts.slice(0, postsToShow);
</script>

<!-- TODO UPDATE THE SEO INFO -->
<Seo title="Ron Bronson" description={variables.siteDescription} path="/" openGraphImage=""/>

# Ron Bronson

<h2>Service Design Leadership</h2>

Ron Bronson is a design leader & strategist with deep experience leading digital initiatives from ideation to post-launch. Outside of work, he's a global speaker on service design. His practice is focused around Consequence Design which centers on interaction design harms (aka "dark patterns"), the intersection of technology in spatial experiences, and consumer advocacy in service delivery. He spent the past 4 years at GSA's 18F, most recently as head of one of the government's largest in-house design teams.

He was appointed by the Mayor to serve on the Portland Historic Landmarks Commission; was a member of several non-profit boards (AIGA Indy, IxDA) and even a community radio station. He started Indianapolis Design Week in 2017, and one summer in Connecticut (accidentally) <a href="https://en.wikipedia.org/wiki/Tennis_polo">invented a sport.</a> Many moons ago, Ron served in US Air Force. <br>

Outside of work, you can also find him spinning up skeeball leagues, curating the tea menu at your favorite hangout, hosting bar trivia, podcasting, or <a href="https://www.superpesis.fi/uutiset/yhdysvaltalainen-ron-bronson-toteutti-unelmansa-ja-matkusti-suomeen-katsomaan-pesapalloa/">ranting online in Finnish</a> about baseball. (it's a long story...) <br>


<h3>Upcoming Talks</h3> 

FTA Tech Conference - Portland, OR (August 2022)<br />
Portland Design Festival - (October 2022)<br />
Federal CX Leadership Symposium - (October 2022) <br />
Rosenfeld Media Civic Design Conference - (November 2022) <br />
ConveyUX - (May 2023) <br />

<h3>Videos of Ron Talking With his Hands</h3>

Ron has presented at over 50 design & tech events around the world since 2017.

<h3>Recent Talks</h3>
<a href="https://vimeo.com/651801535">IxDA Oslo - Dec 2021</a>
<a href="https://www.surfacingpodcast.com/ron-bronson-transcript">Surfacing Podcast</a> - On Service Design (2021)
<a href="https://open.spotify.com/episode/3Xd9MZ9HdByErb41jb7vUX">ACT-IAC Podcast</a> - Edge Cases & Empathy (2021)
<a href="https://youtu.be/JqguCFiY3KM">Service Design Network Global Conference</a> (2020)
<a href="https://aneventapart.com/event/online-0720#s24059">An Event Apart</a> (2020)
<a href="https://www.youtube.com/watch?v=REUJCWpFOcI">DrupalCon</a> (2018)

<h3>Coaching</h3> 
Outside of tech, Ron has coached tennis programs in his spare time around the country including summer camp programs throughout New England.

Since 2020, he’s been the head girls’ tennis coach at Catlin Gabel School in Portland, Oregon, where he’s compliled a dual meet record of 22-1, and coached the program to the 2022 4A-1A Oregon state title, 2 League titles & 2 District championships. During the 2022 state title season, the team broke the single-season record for wins and have completed back-to-back undefeated league seasons, and the team broke the school record for most state tournament entries with 7. He’s coached a state singles finalist, state singles semi-finalist & the state’s top-seeded doubles team all in 2022. He was selected as 2022 Girls Tennis 4A District 1 Girls Tennis Coach of the Year, and is a finalist for 2022 Oregon 4A-1A Girls Tennis State Coach of the Year.

Before that, Ron served as head boys’ tennis coach at Oregon City High School in 2019 where his team was an OSAA All-State Academic team selection in 2019 while playing in the state’s toughest 6A tennis conference. Prior to that, he spent interimittment time as a collegiate & high school assistant for programs in Illinois and Colorado.

Ron’s career dual meet record as a head coach is currently 40-17-1.

As a player, Ron was a four-year letter winner, captain & all-area doubles honorable mention selection his senior year at Plainfield (NJ) High School, where he was part of three consecutive NJSIAA state playoff teams and a conference championship in 1997, which was the first boys tennis conference title in school history. He played one season of college tennis at Monmouth (IL) College in 2003, where he played both singles (4/5/6) & doubles (2) and served as a team captain.

(He also coached college speech & debate for three seasons, (and started at least two college debate programs, and ghostwrote a student government constitution,) but now he just occasionally a new generation of debaters to his odd judging philosophy.)

<h3>Connect</h3>
<a href="mailto:contact@ronbronson.com">Email</a>
<a href="https://twitter.com/ronbronson">Twitter</a>
<a href="https://linkedin.com/in/ronbronson">Linkedin</a>
<a href="https://ronbronson.medium.com/">Medium</a>
<a href="https://last.fm/user/omnivoreron">Last.fm</a>
<a href="https://glass.photo/ron">Instagram</a>
<a href="https://open.spotify.com/user/ronbronson?si=5ad7335e796f4535"><i class="fa-brands fa-spotify"></i></a>

<!--

## [Recent blog posts](/blog)

{#each blogPosts as blogPost}
<BlogSummary {blogPost} />
{/each} 
-->